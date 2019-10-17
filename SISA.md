# Utilização do SISA
## Objetivo: 
instruir o time a fazer o cadastro dos ativos no SISA no padrão definido 

#### Info pertinente
- Fazer cadastro com LETRAS MAIUSCULAS 
- Se a maquina não tiver placa de ativo, usar o seguinte padrão *semativo* + ServiceTag do equipamento
#### Usuário para estoque e desktop:
- Para atribuir um desktop utilizar o user: SamaraINFRA
- Ativos que não possuem nenhuma atribuição são considerados estoque.

#### No campo *Marcação do ativo* nós vamos especificar a empresa de origem para que não haja duplicidade.
###### *Por exemplo*
- Se o ativo for Ex Zap iremos fazer o cadastro nesse padrão, Z de zap e o numero do ativo. Ex: *Z000234
- Se o ativo for Ex Viva seguimos com o mesmo padrão, V de Viva e o numero do ativo. Ex: *V000234
- E assim vai variando conforme a empresa de origem do ativo;

## Campos obrigatorios para criação de um ativo:
- *Empresas* 
- *Marcação do Ativo* 
- *Modelo*, se for note: (SO, Memória, Processador, Tipo HD e Capacidade)
- *Modelo*, se for Cel: (IMEI e Sistema).             
###### Para cadastrar um Celular 
Colocar o primeiro numero do IMEI no campo *Marcação de ativo* e o segundo no campo *IMEI*
- *Status*
###### Rotulos de status
- *Funcional*,(Você deve selecionar esse status para poder atribuir um ativo funcional para um usuário)
- *Pendente*, (Esses ativos não podem ser atribuídos a ninguém, utilizamos eles para equipamentos quebrados porém que tem reparo ou garantia)
- *Irrecuperável*, (usamos ele para itens que vamos descartar ou que não utilizamos mais)

###### E por ultimo o Local

- *Local Padrão* , (Preencher de acordo com a localidade que o equipamento vai ficar).


