# Consultas Online 

# Sumário

### 1.COMPONENTES<br>
João Pedro Ferreira Silva ( Joaopedro.ferreirasilva@outlook.com) <br>

### 2.INTRODUÇÃO E MOTIVAÇAO<br>

A melhoria da saúde pública é um desses grandes desafios que o Brasil precisa vencer, principalmente quando avaliamos o Sistema Único de Saúde (SUS).

Para garantir saúde pública de qualidade a toda população, o Brasil ainda precisa percorrer um longo caminho. A falta de médicos em regiões afastadas em contraponto à intensa concentração nas grandes cidades, além da dificuldade em conseguir atendimento no SUS são apenas alguns dos inúmeros problemas que atingem os brasileiros que tentam utilizar a saúde pública diariamente. 

Para tentar amenizar um pouco desse problema, que é a crescente demora e dificuldade de conseguir atendimento no SUS, pensamos em aplicativo que pode tornar muito mais fácil a qualquer um que o tenha de ser atendido.

A pessoa que obtiver esse aplicativo em mãos poderá marcar sua consulta ou exame em algum horário de sua preferência ( desde que esse horário esteja disponível para o médico em questão. Isso fará com que o cliente não fique esperando em filas para marcar sua consulta ou que não dependa de terceiros para marcarem em uma hora inconveniente.  Esse aplicativo tornará a marcação de consultas e exames, em geral, muito mais prática, simples e pertinente.


<br>

### 3.MINI-MUNDO<br>


O aplicativo foi criado com o objetivo de facilitar a marcação de consulta e torná-la mais simples. O paciente terá mais facilidade para agendar a especialidade que necessita. No consultafast poderá ser encontrado o prontuário do paciente, a Classificação Internacional de Doenças - CID 10, lembretes e observações, chat com médicos e outros pacientes mediante uma rede interna, biblioteca com listagem de todos os medicamentos e fórmulas, remédios caseiros, exames e relatórios integrados ao perfil do paciente, também será possível a marcação de exames, além do mais terá dicas de prevenção de doenças e de primeiros socorros, mostrará hospitais e postos de saúde mais próximos do paciente, contando também com uma função de emergência, no qual o paciente envia a localização para que seja atendido pela ambulância mais próxima. O aplicativo conta ainda com mensagens enviadas ao paciente para lembrá-lo de suas consultas de modo que não se esqueçam das consultas. 

Para a marcação de consultas o paciente entrará com os dados: nome, login, senha, sexo, número de telefone, data a nascimento, endereço, etc. Quando o paciente for entrar na sua conta no sistema, ele deverá escolher a opção de "logar como paciente" e somente assim será exigido seu login e senha. Os dados do paciente ficaram armazenados podendo ser editados a qualquer momento. 

Os médicos também deverão ser cadastrados no , sistema. Devendo inserir endereço, telefone, data de nascimento, sexo, especialidade, número de registro e clínica no qual atua. A clinica para ser cadastrada, também deverá inserir os dados como nome, endereço, cnpj, telefone e planos atendidos na mesma. O médico após a ter realizado o cadastro será capaz de fazer o login em sua conta e editar as informações de seu perfil. Podendo apenas um paciente por horário. O paciente tem a possibilidade de desmarcar e assim possibilitar que outra pessoa possa marcar e os médicos não fiquem com horários vagos.

### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>



![teste](https://user-images.githubusercontent.com/31417932/30292162-90761878-970b-11e7-9049-ba2c5685ae3a.jpg)


### 5.MODELO CONCEITUAL<br>
![gftgg](https://user-images.githubusercontent.com/26657007/33724674-3956bdd2-db57-11e7-9a0b-ba10f1fdd59e.png)




#### 5.2 DECISÕES DE PROJETO
     
    Tabela Pessoas: Optamos por deixar essa tabela como pai e fazer das tabelas médico, paciente é clinica, herdarem dela algumas caracteristicas, por que ambas as três, tem coisas em comuns.
    Tabela Endereço: Optamos por colocar um campo multivalorado e composto, pois cada medico e cada clinica tem seu proprio endereço, é também acrescentar tabelas de bairro, cidade e estado, para que não tenha conflito no futuro, pois podem existir vários endereços com mesmo nome ou número ou cidade identicos.
    Tabela contatos: Optamos por isso devido ao fato de cada pessoa pode ter 1 ou mais contatos, ou seja, facilitaria a vida dela com isso, e a tabela tipo de contato que e a extensão dessa tabela, mas ela só armazena os tipos de cada contato.
    Tabela Consulta: Optmanos por deixar essa tabela para obter e fornecer o hórario das consultas.
    
    
#### 5.3 DESCRIÇÃO DOS DADOS 

    PESSOAS : Tabela que armazena as informações da herança que tanto o paciente quanto o médico poderá ter.
    - Campo ID_Pssa: Será utilizado como identificador de cada pessoa.
    - Campo Nome: Será utilizado para obter os dados do nome da pessoa.
    - Campo Login: Será utilizado para obter o login que cada pesssoa irá criar.
    - Campo Senha: Será utilizado para obter a senha que cada pessoa irá conter para poder usar o aplicativo.
    - Campo Rg: Será utilizado para obter o rg de cada pessoa.
    - Campo Cpf: Será utilizado para obter o cpf de cada pessoa .
    - Campo Sexo: Será utilizado para saber se a pessoa e um homem ou mulher.
    - Campo Data_Nsc: Será utilizado para obter a data de nascimento da pessoa que irá utilizar o nosso aplicativo.
    
    PACIENTE: Tabela que armazena as informações relativas ao cliente.
    - Campo ID_User: Será utilizado como identificador de cada paciente.
    - Campo Plano_Sd: Será utilizado para obter o plano e saúde do paciente.
    
    MÉDICO : Tabela que contém as informações relativas ao médico.
    - Campo ID_Medic: Será utilizado como identificador de cada paciente.
    - Campo Crm: Será utilizado para obter o crm do médico.
    - Campo Esp: Será utilizado para se obter a especialidade que o médico atua.
    - Campo Ada: Será utilizado para se obter a área de atuação de cada médico.
   
    CONSULTAS : Tabela que contém as informações necessárias a serem fornecidas sobre cada consulta que será realizada.
    - Campo Horario: Será utilizado para obter e fornecer o hórario das consultas.
    
    CLINICA : Tabela que armazena as informações relativas a clínica onde o cliente fará sua consulta.
    - Campo ID_Clinica: Será utilizado como identificador de cada Clinica.
    
    CONTATO : Tabela que tem os contatos e está ligada a uma sub tabela que e especifica para tipos de contatos.
    - Campo ID_Contato: Será utilizado como identificador de cada Contato.
    - Campo Descrição: Será utilizado para poder dar descrisções sobre seu contato
    - Campo ID_Pssa: Só contém nessa tabela para mostrar que cada pessoa pode ter um tipo de contato.
    - Sub tabela TipoCont ( tipo = telefone, email, sinal de fumaça e etc ).
    
    ENDEREÇO : Tabela que contém as informações do endereço do médico, do cliente e da clinica.
    - Campo ID_Ende: Será utilizado como identificador de cada Endereço.
    - Campo logradouro: Será utilizado para saber se o endereço se localiza em uma rua, ou avenida e etc.
    - Campo Número: Será utilizado para obter o número da clinica.
    - Campo Cep: Será utilizado para obter o número clinica.
    - Sub tabela Bairro:
        - Campo ID_Bairro: Será utilizado como identificador de cada Bairro.
        - Campo Bairro: Será utilizado para obter o Bairro onde se localiza a clinica.
    - Sub tabela Cidade:
        - Campo ID_Cidade: Será utilizado como identificador de cada Cidade.
        - Campo Cidade: Será utilizado para obter o Cidade onde se localiza a clinica.
     - Sub tabela Estado:
       - Campo ID_Estado: Será utilizado como identificador de cada Estado.
       - Campo Estado: Será utilizado para obter o Estado onde se localiza a clinica.
    
    
    

### 6	MODELO LÓGICO<br>

![sdsds](https://user-images.githubusercontent.com/26657007/33726423-263982de-db5c-11e7-85b1-a2509cd5d448.png)




### 7	MODELO FÍSICO<br>

[Fisíco.txt](https://github.com/discipbdtec/Trabalho01/files/1540543/Fisico.txt) 
 
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>

[Insert.txt](https://github.com/discipbdtec/Trabalho01/files/1553757/Insert.txt)

#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        
        a) obtenção dos dados:
        
        Dados obtidos atravéz de tabelas de outros bancos com nomes, epecialidade e outros dados. Endereços obtidos no google maps no estado do Espíto Santo
        
        b) obtenção de códigos reutilizados:
        
        Não teve códigos reutilizados
        
        c) fontes de estudo para desenvolvimento do projeto:
        
        Aulas de BD em sala de aula e tutorias da internet
        
#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) inclusão das instruções para criação das tabelas e estruturas de amazenamento do BD
[Fisíco.txt](https://github.com/discipbdtec/Trabalho01/files/1540543/Fisico.txt)

        b) inclusão das instruções de inserção dos dados nas referidas tabelas
[Insert.txt](https://github.com/discipbdtec/Trabalho01/files/1553757/Insert.txt)



        
### 9	TABELAS E PRINCIPAIS CONSULTAS<br>


#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>


    SELECT * FROM ENDEREÇO

![endereco](https://user-images.githubusercontent.com/31863030/33741189-8731148e-db8a-11e7-9e5c-8b5bf3f50d8d.png)

    SELECT * FROM PACIENTE

![paciente](https://user-images.githubusercontent.com/31863030/33741354-132c7118-db8b-11e7-8f4d-f94d2b2b0b48.png)

    SELECT * FROM MÉDICO

![medico](https://user-images.githubusercontent.com/31863030/33741305-ec2fb9da-db8a-11e7-8add-11ef1f470918.png)

    SELECT * FROM PESSOA

![pessoa](https://user-images.githubusercontent.com/31863030/33741384-39a0071a-db8b-11e7-83d3-98c78b7fde70.png)

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 3) <br>


    select * from Médico
    where Esp = 'cirurgião'

![endereco](https://user-images.githubusercontent.com/31863030/33741738-b1fd2e4e-db8c-11e7-98d8-5797cf58ce3a.png)

    select * from paciente
    where Plano_SD > 100000;

![pl s](https://user-images.githubusercontent.com/31863030/33741708-8fc57e76-db8c-11e7-8c6f-abbda2cc1e9a.png)

    select * from endereço 
    where Logradouro = 'rua'

![lo](https://user-images.githubusercontent.com/31863030/33741651-65006d40-db8c-11e7-9dd8-1ca5c9ec1860.png)


#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E CAMPOS RENOMEADOS (Mínimo 2)<br>

    select avg(horario) from consultas

![me](https://user-images.githubusercontent.com/31863030/33742014-aa9821e4-db8d-11e7-9f17-4e5ca67b6d70.png)

    select sum(Número) from endereço 

![su](https://user-images.githubusercontent.com/31863030/33741966-8b4de49a-db8d-11e7-89c4-688b9bac901a.png)

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE (Mínimo 3)  <br>


    select * from médico where Esp like "c%"

![lk](https://user-images.githubusercontent.com/31863030/33742306-ea853b4c-db8e-11e7-8ca7-a219d95d1b67.png)

    select * from pessoa where nome like "m%"

![lk p](https://user-images.githubusercontent.com/31863030/33742351-1af30c5a-db8f-11e7-8623-163f3deae2cb.png)

    select cep from endereço where logradouro like "r%"

![lk cep](https://user-images.githubusercontent.com/31863030/33742371-32ed8d3a-db8f-11e7-9e1a-dfec309241de.png)

#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>


    update médico set Esp = 'Cardiologista' where ID_Medic = 45438;

![up ende2](https://user-images.githubusercontent.com/26657007/33916285-29d2bfaa-df8f-11e7-8c45-beef875f2cf3.png)
![up ende1](https://user-images.githubusercontent.com/26657007/33916284-29a15398-df8f-11e7-9f88-76d4530b7e8c.png)
    
    update paciente set Plano_Sd = '346000' where ID_User = 450445;

![up pct](https://user-images.githubusercontent.com/26657007/33916339-658e348e-df8f-11e7-8c58-fce6fd7111da.png)
![up pct1](https://user-images.githubusercontent.com/26657007/33916340-65c9b126-df8f-11e7-91a5-581a93ced386.png)

    update endereço set Número = '150' where ID_Ende = 100;

![up medi](https://user-images.githubusercontent.com/26657007/33916312-47941a3e-df8f-11e7-9d99-998c2b62a4dc.png)
![up medi1](https://user-images.githubusercontent.com/26657007/33916313-47c606e8-df8f-11e7-8890-0430ef216eac.png)

    delete from paciente where FK_Pessoa_ID_Pssa = 3002 ;

![delpac1](https://user-images.githubusercontent.com/26657007/33916496-4fa30e14-df90-11e7-8905-2f54a654e604.png)
![delpac2](https://user-images.githubusercontent.com/26657007/33916495-4f73b4a2-df90-11e7-93f7-176bcf9704ba.png)

    delete from médico where ID_Medic= 45437;

![delmedic1](https://user-images.githubusercontent.com/26657007/33916535-802c6f3a-df90-11e7-89d9-fb3d4ea35dfb.png)
![delmedic2](https://user-images.githubusercontent.com/26657007/33916536-805edf9c-df90-11e7-8ef7-7102ca6cea8e.png)

    delete from endereço where ID_Ende = 103;
    
![delende1](https://user-images.githubusercontent.com/26657007/33916525-70959eca-df90-11e7-870b-7e1bfa166fec.png)
![delende2](https://user-images.githubusercontent.com/26657007/33916526-70c54d32-df90-11e7-89ba-13ef6a40b2f7.png)


#### 9.6	CONSULTAS COM JUNÇÃO (Todas Junções)<br>


    select nome,ID_pssa from pessoa
    inner join médico
    on (pessoa.ID_Pssa = médico.FK_Pessoa_ID_Pssa)

![join](https://user-images.githubusercontent.com/31863030/33743010-283b14d6-db92-11e7-84c3-a78ea7d9caee.png)

    select pessoa.nome, contato.descrição from pessoa
    inner join contato
    on (pessoa.ID_Pssa = contato.ID_pssa)

![join2](https://user-images.githubusercontent.com/31863030/33743040-4106307c-db92-11e7-9e04-eadf9f001bb3.png)

    select pessoa.nome, paciente.Plano_Sd from pessoa
    inner join paciente
    on (pessoa.ID_pssa = paciente.FK_Pessoa_ID_pssa)

![join3](https://user-images.githubusercontent.com/31863030/33743063-5ac3b2f0-db92-11e7-970c-0788b3525336.png)

#### 9.7	CONSULTAS COM GROUP BY (Mínimo 5)<br>


    select * from pessoa group by sexo

![group](https://user-images.githubusercontent.com/31863030/33743315-749297b8-db93-11e7-805d-ba94bba79e26.png)

    select * from endereço group by logradouro

![group2](https://user-images.githubusercontent.com/31863030/33743351-95a2ed54-db93-11e7-8d2f-d53592ad6762.png)

    select * from pessoa group by Data_Nsc

![group3](https://user-images.githubusercontent.com/31863030/33743367-b0554d0e-db93-11e7-936f-c70220a54844.png)

    select * from pessoa group by nome;
    
![group by nome](https://user-images.githubusercontent.com/26657007/33915713-eb42b478-df8b-11e7-8c1d-9f3e9d6dc9cc.png)
    
    select * from endereço group by número;
    
![group by numero](https://user-images.githubusercontent.com/26657007/33915743-07a2e8f4-df8c-11e7-8438-b7ad82d21946.png)
    

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4) <br>


    select pessoa.nome, contato.descrição from pessoa left outer join contato on (pessoa.ID_Pssa = contato.ID_pssa)

![left](https://user-images.githubusercontent.com/31863030/33743560-7ce8ab04-db94-11e7-9557-c8b4f4cc743c.png)

    
    select pessoa.nome, paciente.Plano_Sd from pessoa left outer join paciente on (pessoa.ID_pssa = paciente.FK_Pessoa_ID_pssa)

![left2](https://user-images.githubusercontent.com/31863030/33743582-9c04c694-db94-11e7-87e1-8eb6d26d3bde.png)

    
    select pessoa.nome, paciente.Plano_Sd from pessoa right outer join paciente on (pessoa.ID_pssa = paciente.FK_Pessoa_ID_pssa)

![right](https://user-images.githubusercontent.com/31863030/33743672-fb7ab75a-db94-11e7-9034-b42f438a096e.png)

    
    select pessoa.nome, contato.descrição from pessoa right outer join contato on (pessoa.ID_Pssa = contato.ID_pssa)

![right2](https://user-images.githubusercontent.com/31863030/33743715-1ffeebc8-db95-11e7-9154-f6cbfa9b530f.png)


#### 9.9	CONSULTAS COM SELF JOIN (todas) E VIEW (mais importantes) <br>

    create view usuarios as
    select count(*) as usuarios from paciente;
    select * from usuarios;
    
![user](https://user-images.githubusercontent.com/26657007/33915837-a6878c0e-df8c-11e7-8337-4ea3635d9357.png)
    
    create view clientesTotal as
    select count(*) as clientesTotal from pessoa;
    select * from clientesTotal;
    
![clientes](https://user-images.githubusercontent.com/26657007/33915835-a60718bc-df8c-11e7-9e48-e2d5f32d93fa.png)

    create view EndTote as
    select count(*) as EndTote from endereço;
    select * from EndTote;

![ende](https://user-images.githubusercontent.com/26657007/33915836-a63e2fd2-df8c-11e7-972b-838ee8beac5d.png)




#### 9.10	SUBCONSULTAS (Mínimo 3) <br>

    select * from pessoa where sexo in ("masculino")

![masculino](https://user-images.githubusercontent.com/26657007/33916067-1ecb9312-df8e-11e7-81a0-89d4bb0ddb76.png)

    
    select * from endereço where logradouro in ('rua')

![rua](https://user-images.githubusercontent.com/26657007/33916068-1f18941e-df8e-11e7-92f5-ab1759b4eaa2.png)

    
    select * from médico where esp in (select esp from médico where esp = 'Fisioterapeuta')

![fisio](https://user-images.githubusercontent.com/26657007/33916065-1e9eff96-df8e-11e7-829a-e9c043cb0858.png)

#####################################################


### 11	DIFICULDADES ENCONTRADAS PELO GRUPO<br>

        Houve dificuldade na relação de tabelas e cardinalidade entre elas.
        Vários problemas de relacionamento de tabelas, principalmente nas de endereço e contato.
        Houve também dificuldade para fazer as heranças, dividir em pessoa fisica e juridica.
        Dificuldade para rodar o físico no SQL.
        Vários problemas em relação ter que mudar uma coisa no modelo conceitual e ter que mudar todo trabalho, ou mudar o fisico e refazer tod o trabalho também.




#####################################################


### Requisitos

    Caso 1 - Medico
    RF001 : Cadastrar médico
    RNF001: Mostrar perfil
    RF002 : Fazer login
    RF003 : Disponibilizar horários

    Caso 2 - Cliente
    RF004: Cadastrar cliente
    RF005 : Fazer login
    RF006: Buscar consultório e buscar medico
    RF006: Marcar consulta / exame
    RF007: Desmarcar consulta / exame
    RNF002: Mostrar perfil
    RNF005: Visualizar horários disponíveis



####  Casos de Uso

![diagrama casos de uso](https://user-images.githubusercontent.com/26657007/33725848-8a1c4da6-db5a-11e7-8de0-e72a8f0a42e8.png)


### Sequência

![diagrama de sequencia](https://user-images.githubusercontent.com/26657007/33725850-8a69bda2-db5a-11e7-9c73-cd68969f56e4.png)


### Atividades

![diagrama de atividades](https://user-images.githubusercontent.com/26657007/33725849-8a44ec3e-db5a-11e7-9911-33d21afb19cf.png)


    
