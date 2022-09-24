# Database Experiênce

## O que é Sql e NoSql?

Banco de dados Relacional (Sql) é um conjunto de dados em que tem um relacionamento entre si.

Banco de dados Não Somente Relacional (NoSql) foi criado para necessidades de armazenar um volume cada vez maior e também manter informações não estruturadas, estrutura que não conhecemos. Não foram criados para a substuição do SQL e sim um complemento a eles.

> Demanda de Dados

Com o conceito de trabalho distribuído, o time engenharia de dados trabalha bem proximo dos times de negócio fortalecendo, através dos conhecimentos técnicos os motivos de criação de cada indicador criado para tirar insights daquele contexto/área específica.

### Resumo MongoDB

MongoDB é um sistema de gerenciamento de banco de dados não relacional NoSQL, bastante conhecido, e que armazena dados em forma de documentos BSON (JSON binário). Muito utilizado no campo de big data e aplicativos onde a necessidade de execução em tempo real é primordial para seu funcionamento. Relativo ao teorema CAP, o MongoDB é um armazenamento de dados CP ou seja, resolve partições de rede mantendo a consistência, porém não oferece a disponibilidade constante. Existem outras alternativas de bancos NoSQL que oferecem pilares diferentes do sistema CAP, como por exemplo o Cassandra, que por si só garante os pilares AP.
Um cluster MongoDB é composto por dois tipos de membros portadores de dados sendo eles:
Primário: É um nó principal mestre que recebe todas as operações de gravação.
Secundário: Recebe apenas os dados replicados do nó principal para manter um conjunto de dados idênticos.
Por padrão o membro principal lida com todas as leituras e gravações, porém é possível realizar alterações para que haja a possibilidade de leitura de alguma ou todas as informações pelo membro secundário. A regra é que as gravações sempre devem ser enviadas ao membro primário. Se houver falhas no membro principal todas as gravações serão suspensas até que o novo membro primário seja selecionado. De acordo com a documentação do MongoDB, esse processo pode levar até 12 segundos para ser concluído.
Para aumentar essa disponibilidade, podemos lidar com recursos citados anteriormente, onde distribuímos o cluster através de data centers geograficamente distintos. Ainda assim, temos limitações nesse processo onde o tamanho máximo de réplicas de nós do MongoDB está limitado a 50.
