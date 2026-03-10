```mermaid
graph TD
    Developer[Desenvolvedor] --> GitRepo[Git Repository]
    GitRepo --> CICD[CI Pipeline]
    CICD --> ArtifactRepo[Artifact Repository]
    ArtifactRepo --> Container[Container Image]
    Container --> CloudRuntime[Cloud Runtime]

    ExternalAttacker[Ataque externo] --> API[API]
    ExternalAttacker --> WebApp[Aplicação Web]
    ExternalAttacker --> CICD

    Dependências[Dependências] --> GitRepo
    OpenSource[Pacotes opensource] --> Dependências
    MaliciousPackage[Pacote malicioso] --> Dependências

    Secrets[Secrets] --> GitRepo
    Secrets --> CICD
    Secrets --> CloudRuntime
