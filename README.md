
# InfoCorpProject

## Descrição do Projeto
O **InfoCorpProject** é um sistema de gerenciamento de pedidos que implementa funcionalidades relacionadas a usuários, perfis, produtos, pedidos, itens de pedidos e pagamentos. O projeto utiliza **JPA** e **Hibernate** para mapeamento objeto-relacional, garantindo persistência de dados em um banco relacional.

## Estrutura do Projeto

1. **Usuario**: Representa os usuários do sistema.
2. **Perfil**: Representa os perfis associados aos usuários.
3. **Produto**: Representa os produtos disponíveis para pedidos.
4. **Pedido**: Representa os pedidos realizados pelos usuários.
5. **ItemPedido**: Representa os itens que compõem cada pedido.
6. **Pagamento**: Representa os pagamentos realizados para os pedidos.


## Funcionalidades Principais
### Usuários e Perfis
- Gerenciamento de usuários com informações como nome, e-mail, telefone e senha.
- Associação de múltiplos perfis a cada usuário (ex.: Admin, Cliente).

### Produtos
- Cadastro de produtos com nome, descrição, preço e quantidade em estoque.
- Controle automático de data de cadastro.

### Pedidos
- Realização de pedidos por usuários.
- Associação de itens de pedidos a produtos com controle de quantidade e preço.

### Pagamentos
- Registro de pagamentos para pedidos.
- Controle de métodos de pagamento (ex.: cartão de crédito, boleto).
- Data automática de registro do pagamento.

## Configuração do Projeto

### Pré-requisitos
- **Java 8+**
- **Maven**
- **Banco de Dados Relacional** (ex.: MySQL, PostgreSQL)
- **IDE** (ex.: IntelliJ IDEA, Eclipse)

### Passos para Configurar
1. **Clone o repositório**:
2. **Importe o projeto na sua IDE** como um projeto Maven.
3. **Configure o arquivo `application.properties`**:
   - Insira as configurações do banco de dados, como URL, usuário e senha.
   - Exemplo:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/infocorp
     spring.datasource.username=seu_usuario
     spring.datasource.password=sua_senha
     spring.jpa.hibernate.ddl-auto=update
     ```
4. **Execute o projeto** na sua IDE ou via Maven:
   ```bash
   mvn spring-boot:run
   ```

---

## Estrutura das Entidades

1. **Usuario ↔ Perfil**: Muitos-para-muitos.
2. **Pedido ↔ Usuario**: Muitos-para-um.
3. **Pedido ↔ ItemPedido**: Um-para-muitos.
4. **ItemPedido ↔ Produto**: Muitos-para-um.
5. **Pedido ↔ Pagamento**: Um-para-um.

Cada classe está mapeada com **JPA** e utiliza anotações como `@Entity`, `@Table`, `@ManyToOne`, `@OneToMany`, e outras.

---

## Documentação de Código
Para uma visão detalhada das classes e funcionalidades, consulte a **[Documentação das Classes](#)**.


Esse `README.md` oferece uma visão geral bem detalhada do projeto, incluindo descrição, configuração, funcionalidades principais e como rodar o projeto. Caso precise ajustar algum detalhe ou adicionar algo específico, é só me informar!
