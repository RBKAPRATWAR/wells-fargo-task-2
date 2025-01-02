# Task 2 Starter Repo
Contains Everything you need to get started on task 2 of Forage's Wells Fargo software engineering program
import jakarta.persistence.*;
import java.util.List;

@Entity
public class FinancialAdvisor {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long advisorId;

    private String name;
    private String email;
    private String phoneNumber;

    @OneToMany(mappedBy = "financialAdvisor", cascade = CascadeType.ALL)
    private List<Client> clients;

    // Getters and setters
}
