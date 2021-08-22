---
title: Sintaxe de consulta avançada
description: a sintaxe de consulta avançada (AQS) é usada pelo Microsoft Windows Desktop Search (WDS) para ajudar os usuários e os programadores a definir e restringir melhor suas pesquisas.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 2daf552f8f750335abacea4b550f92bd71c91c9b2b688a387b035a8180a8b3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601816"
---
# <a name="advanced-query-syntax"></a>Sintaxe de consulta avançada

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use [Windows pesquisa](../search/-search-3x-wds-overview.md) em vez disso.

a sintaxe de consulta avançada (AQS) é usada pelo Microsoft Windows Desktop Search (WDS) para ajudar os usuários e os programadores a definir e restringir melhor suas pesquisas. Usar o AQS é uma maneira fácil de restringir as pesquisas e fornecer melhores conjuntos de resultados. As pesquisas podem ser limitadas pelos seguintes parâmetros:

-   Tipos de arquivo: pastas, documentos, apresentações, imagens e assim por diante.
-   Armazenamentos de arquivos: bancos de dados e locais específicos.
-   Propriedades do arquivo: tamanho, data, título e assim por diante.
-   Conteúdo do arquivo: palavras-chave como "resultados finais do projeto", "AQS", "Suede azul" e assim por diante.

Além disso, os parâmetros de pesquisa podem ser combinados usando operadores de pesquisa. O restante desta seção explica a sintaxe de consulta, os parâmetros e os operadores e como eles podem ser combinados para oferecer resultados de pesquisa direcionados. as tabelas descrevem a sintaxe a ser usada com o WDS, bem como as propriedades que podem ser consultadas para cada tipo de arquivo exibido na janela de resultados do **Windows Desktop Search** .

## <a name="desktop-search-syntax"></a>Sintaxe do Desktop Search

Uma consulta de pesquisa pode incluir uma ou mais palavras-chave, com operadores boolianos e critérios opcionais. Esses critérios opcionais podem restringir uma pesquisa com base no seguinte:

-   Escopo ou armazenamento de dados no qual os arquivos residem
-   Tipos de arquivos
-   Propriedades gerenciadas de arquivos

Os critérios opcionais, descritos com mais detalhes a seguir, usam a seguinte sintaxe:

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Suponha que um usuário queira Pesquisar um documento que contenha a frase "último trimestre", criada por João ou Joanne, e que o usuário tenha salvo na pasta MyDocuments. A consulta pode ter a seguinte aparência:

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Escopo: locais e armazenamentos de dados

Os usuários podem limitar o escopo de suas pesquisas a locais de pasta ou armazenamentos de dados específicos. por exemplo, se você usar várias contas de email e quiser limitar uma consulta para o microsoft Outlook ou o microsoft Outlook Express, poderá usar `store:outlook` ou `store:oe` respectivamente.



| Restringir pesquisa por repositório de dados | Uso              | Exemplo                                  |
|-------------------------------|------------------|------------------------------------------|
| Desktop                       | área de trabalho          | loja: área de trabalho                            |
| Arquivos                         | files            | armazenar: arquivos                              |
| Outlook                       | outlook          | loja: Outlook                            |
| Outlook Express               | oe               | Store: OE                                 |
| Pasta específica               | nome_da_pasta ou in | nome_da_pasta: mydocumentações ou em: MyDocuments |



 

Se você tiver um manipulador de protocolo para rastrear repositórios personalizados, como o Lotus Notes, você poderá usar o nome da loja ou do manipulador de protocolo para o repositório. Por exemplo, se você implementou um manipulador de protocolo para incluir um armazenamento de dados do Lotus Notes como "Observações", a sintaxe da consulta seria `store:notes` .

### <a name="common-file-kinds"></a>Tipos de arquivo comuns

Os usuários também podem limitar suas pesquisas a tipos específicos de arquivos, chamados tipos de arquivos. A tabela a seguir lista os tipos de arquivo e oferece exemplos da sintaxe usada para pesquisar esses tipos de arquivos.



| Para restringir por tipo de arquivo:       | Uso              | Exemplo                        |
|---------------------------------|------------------|--------------------------------|
| Todos os tipos de arquivo                  | –       | espécie: tudo                |
| Comunicações                  | comunicações   | espécie: comunicações            |
| Contatos                        | contatos         | tipo: contatos                  |
| Email                          | email            | tipo: email                     |
| Conversas do Instant Messenger | Mi               | tipo: im                        |
| Encontros                        | encontros         | espécie: reuniões                  |
| Tarefas                           | tarefas            | tipo: tarefas                     |
| Observações                           | HDInsight            | tipo: observações                     |
| Documentos                       | docs             | tipo: docs                      |
| Documentos de texto                  | texto             | tipo: texto                      |
| Planilhas                    | planilhas     | tipo: planilhas              |
| Apresentações                   | apresentações    | tipo: apresentações             |
| Música                           | music            | tipo: música                     |
| Imagens                        | classificação pics             | tipo: imgs                      |
| vídeos                          | Vídeos           | tipo: vídeos                    |
| Pastas                         | pastas          | tipo: pastas                   |
| Nome da pasta                     | nome_da_pasta ou in | nome_da_pasta: mydocs ou in: mydocs |
| Favoritos                       | favoritos        | tipo: favoritos                 |
| Programas                        | programas         | tipo: programas                  |



 

### <a name="boolean-operators"></a>Operadores boolianos

As palavras-chave de pesquisa e as propriedades do arquivo podem ser combinadas para ampliar ou restringir uma pesquisa com operadores. A tabela a seguir explica os operadores comuns usados em uma consulta de pesquisa.



| Palavra-chave/símbolo  | Exemplos                                              | Função                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NOT             | Não segurança social<br/>                        | Localiza itens que contêm *redes sociais*, mas não *segurança*.<br/>                                              |
|                 | segurança social<br/>                           | Localiza itens que contêm *redes sociais* e de *segurança*.<br/>                                              |
| OU              | social ou de segurança<br/>                         | Localiza itens que contêm *redes sociais* ou de *segurança*.<br/>                                                    |
| Aspas | "segurança social"<br/>                          | Localiza itens que contêm a frase de *segurança social* exata.<br/>                                        |
| Parênteses     | (segurança social)<br/>                          | Localiza itens que contêm *redes sociais* e de *segurança* em qualquer ordem.<br/>                                      |
| >            | Data: >11/05/04<br/> Tamanho: >500<br/>  | Localiza itens com uma data após 11/05/04. <br/> Localiza itens com um tamanho maior que 500 bytes.<br/> |
| <            | Data: <11/05/04 <br/> Tamanho: <500<br/> | Localiza itens com uma data anterior a 11/05/04. <br/> Localiza itens com um tamanho menor que 500 bytes.<br/>   |
| ..              | Data: 11/05/04.. 11/10/04<br/>                    | Localiza itens com uma data começando em 11/05/04 e terminando em 11/10/04.<br/>                               |



 

> [!Note]
>
> Os operadores **não** e **ou** devem estar em letras maiúsculas e não podem ser combinados em uma consulta (por exemplo, `social OR security NOT retirement` ).

 

### <a name="boolean-properties"></a>Propriedades booleanas

Alguns tipos de arquivo permitem que os usuários pesquisem arquivos usando propriedades booleanas, conforme descrito na tabela a seguir.



| Propriedade       | Exemplo                   | Função                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| é: anexo  | o relatório é: anexo      | Localiza itens que têm anexos que contêm *relatório*. Mesmo que `isattachment:true`.                           |
| IsOnline:      | relatório IsOnline: verdadeiro      | Localiza itens que estão online e que contêm *relatórios*.                                                         |
| isrecurring:   | IsRecurring do relatório: verdadeiro   | Localiza itens que são recorrentes e que contêm *relatórios*.                                                       |
| issinalizado:     | relatório issinalizado: verdadeiro     | Localiza itens sinalizados (revisão, acompanhamento, por exemplo) e que contêm *relatórios*.                       |
| IsDeleted     | relatório IsDeleted: true     | Localiza itens sinalizados como excluídos (lixeira ou itens excluídos, por exemplo) e que contêm *relatórios*. |
| Membros IsCompleted   | relatório IsCompleted: false  | Localiza itens que não estão sinalizados como concluídos e que contêm *relatórios*.                                        |
| HasAttachment | HasAttachment do relatório: verdadeiro | Localiza os itens que contêm o *relatório* e os anexos                                                          |
| HasFlag       | HasFlag do relatório: verdadeiro       | Localiza os itens que contêm o *relatório* e os sinalizadores.                                                                |



 

### <a name="dates"></a>Datas

Além de Pesquisar datas específicas e intervalos de datas usando os operadores descritos anteriormente, o AQS permite valores de datas relativas (como `today` , `tomorrow` ou `next week` ) e valores de Day (like `Tuesday` ou `Monday..Wednesday` ) e month ( `February` ).



| Relativo a:    | Exemplo de sintaxe                                                                                                                         | Resultado                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dia             | Data: hoje<br/> Data: amanhã<br/> Data: ontem<br/>                                                               | Localiza itens com a data de hoje.<br/> Localiza itens com a data de amanhã.<br/> Localiza itens com a data de ontem. <br/>                                                                                                                                                                                                                     |
| Semana/mês/ano | Data: esta semana<br/> Data: última semana<br/> Data: próximo mês<br/> Data: último mês<br/> Data: ano passado <br/> | Localiza itens com uma data caindo na semana atual.<br/> Localiza itens com uma data de queda na semana anterior.<br/> Localiza itens com uma data que esteja na próxima semana.<br/> Localiza itens com uma data de queda no mês anterior.<br/> Localiza itens com uma data caindo no próximo ano. <br/> |



 

## <a name="properties-by-file-kind"></a>Propriedades por tipo de arquivo

Os usuários podem pesquisar propriedades específicas de diferentes tipos de arquivo. Algumas propriedades (como o tamanho do arquivo) são comuns a todos os arquivos, enquanto outras são limitadas a um tipo específico. A contagem de slides, por exemplo, é específica para apresentações. As tabelas a seguir listam essas propriedades por tipo de arquivo.

### <a name="file-kind-everything"></a>Tipo de arquivo: tudo

Essas são propriedades comuns a todos os tipos de arquivo. Para incluir todos os tipos de arquivos em uma consulta, a sintaxe é:

`kind:everything <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade       | Uso                      | Exemplo                        |
|----------------|--------------------------|--------------------------------|
| Title          | título, assunto ou sobre  | title:"Quarterly Financial"    |
| Status         | status                   | status:complete                |
| Data           | data                     | date:last week                 |
| Data da modificação  | datemodified ou modified | modified:last week             |
| Importância     | importância ou prioridade   | importance:high                |
| Tamanho           | tamanho                     | size:> 50                   |
| Excluído        | excluído ou isdeletado     | isdeleted:true                 |
| É anexo  | isattachment             | isattachment:true              |
| Para             | para ou paranome             | to:bob                         |
| Cc             | cc ou ccname             | cc:john                        |
| Empresa        | company                  | company:Microsoft              |
| Localização       | local                 | location:"Sala de conferência 102" |
| Categoria       | category                 | category:Business              |
| Palavras-chave       | palavras-chave                 | keywords:"sales projections"   |
| Álbum          | Álbum                    | album:"Fly by Night"           |
| Nome do arquivo      | filename ou file         | filename:MyResume              |
| Gênero          | gênero                    | genre:rock                     |
| Autor         | autor ou por             | author:"Stephen King"          |
| Pessoas         | pessoas ou com           | with:(filhoja ou david)          |
| Pasta         | pasta, em ou caminho    | folder:downloads               |
| Extensão de arquivo | ext ou fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Anexo

Essas são propriedades comuns aos anexos. Para limitar a pesquisa apenas a anexos, a sintaxe é:

`kind:attachment <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade | Uso            | Exemplo                  |
|----------|----------------|--------------------------|
| Pessoas   | pessoas ou com | people:john ou with:john |



 

### <a name="contacts"></a>Contatos

Essas são propriedades comuns aos contatos. Para limitar a pesquisa somente a contatos, a sintaxe é:

`kind:contacts <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade              | Uso                 | Exemplo                            |
|-----------------------|---------------------|------------------------------------|
| Cargo             | jobtitle            | jobtitle:CFO                       |
| Endereço do IM            | imaddress           | imaddress:john\_doe@msn.com        |
| Telefone do assistente     | assistantsphone     | assistantsphone:555-3323           |
| Nome do assistente        | Assistantname       | assistantname:Paul                 |
| Profession            | Profissão          | (10:10000                 |
| Apelido              | apelido            | apelido:Tex                       |
| Cônjuge                | Cônjuge              | 100000011:                      |
| Cidade comercial         | businesscity        | businesscity:Seattle               |
| Cep comercial  | businesspostalcode  | businesspostalcode:98006           |
| Negócios home page    | businesshomepage    | businesshomepage:www.microsoft.com |
| Número de telefone de retorno de chamada | callbackphonenumber | callbackphonenumber:555-555-2121   |
| Telefone do carro             | Carphone            | carphone:555-555-2121              |
| Children              | menores de idade            | children:T ltd                     |
| Nome            | nome           | firstname:John                     |
| Sobrenome             | sobrenome            | lastname:Doe                       |
| Fax em casa              | homefax             | homefax:555-555-2121               |
| Nome do gerente        | managersname        | managersname:John                  |
| Pager                 | pager               | pager:555-555-2121                 |
| Telefone comercial        | businessphone       | businessphone:555-555-2121         |
| Telefone residencial            | homePhone           | homephone:555-555-2121             |
| Telefone celular          | Celular         | mobilephone:555-555-2121           |
| Office                | Office              | office:sample                      |
| Aniversário           | Aniversário         | anniversary:1/1/06                 |
| Birthday              | Aniversário            | aniversário:1/1/06                    |
| Página da Web              | página da web             | webpage:www.microsoft.com          |



 

> [!Note]
>
> Telefone números são indexados como inseridos. Por exemplo, se um usuário não incluiu um código de país ou área ao inserir o número de telefone, os usuários não poderão localizar um contato se pesquisar com o código de país ou área no número de telefone.

 

### <a name="communications"></a>Comunicações

Essas são propriedades comuns às comunicações. Para limitar a pesquisa somente às comunicações, a sintaxe é:

`kind:communications <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade       | Uso                           | Exemplo                         |
|----------------|-------------------------------|---------------------------------|
| De           | de ou organizador             | from:john                       |
| Recebido       | recebido ou enviado              | sent:ontem                  |
| Assunto        | assunto ou título              | subject:"Quarterly Financial"   |
| Tem anexo | hasattachments, hasattachment | hasattachment:true              |
| Anexos    | anexos ou anexos     | attachment:presentation.ppt     |
| Cco            | bcc, bccname ou bccaddress    | bcc:dave                        |
| Endereço cc     | ccaddress ou cc               | ccaddress:john\_doe@outlook.com |
| Sinalizador de acompanhamento | followupflag                  | followupflag:2                  |
| Data de vencimento       | duedate ou due                | due:last week                   |
| Ler           | leitura ou leitura                | is:read                         |
| Foi concluído   | Iscompleted                   | is:completed                    |
| Incompleto     | incomplete ou isincomplete    | is:incomplete                   |
| Tem sinalizador       | hasflag ou isflagged          | has:flag                        |
| Duração       | duration                      | duration:> 50                |



 

### <a name="calendar"></a>Calendário

Essas são propriedades comuns aos calendários. Para limitar a pesquisa apenas a calendários, a sintaxe é:

`kind:calendar <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade  | Uso                      | Exemplo          |
|-----------|--------------------------|------------------|
| Recorrente | recorrente ou recorrente | is:recurring     |
| Organizer | organizador, por ou de    | organizer:ltd |



 

### <a name="documents"></a>Documentos

Essas são propriedades comuns a documentos. Para limitar a pesquisa apenas a documentos, a sintaxe é:

`kind:documents <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade          | Uso             | Exemplo                       |
|-------------------|-----------------|-------------------------------|
| Comentários          | comments        | comments:"needs final review" |
| Último salvo por     | lastsavedby     | lastsavedby:john              |
| Gerenciador de documentos  | documentmanager | documentmanager:john          |
| Número de revisão   | Revisionnumber  | revisionnumber:1.0.3          |
| Formato do documento   | documentformat  | documentformat:MIMETYPE       |
| Data da última impressa | datelastprinted | datelastprinted:last week     |



 

### <a name="presentation"></a>Apresentação

Essas são propriedades comuns às apresentações. Para limitar a pesquisa somente a apresentações, a sintaxe é:

`kind:presentation <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade    | Uso        | Exemplo           |
|-------------|------------|-------------------|
| Contagem de slides | slidecount | slidecount:>20 |



 

### <a name="music"></a>Música

Essas são propriedades comuns a arquivos de música. Para limitar a pesquisa apenas à música, a sintaxe é:

`kind:music <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade | Uso                | Exemplo                  |
|----------|--------------------|--------------------------|
| Taxa de bits | taxa de bits, taxa      | taxa de bits:192              |
| Artista   | artist, by ou from | artist:John John       |
| Duração | duration           | duration:3               |
| Álbum    | Álbum              | album:"greatest hits"    |
| Gênero    | gênero              | genre:rock               |
| Rastrear    | rastrear              | track:12                 |
| Year     | ano               | year:> 1980 < 1990 |



 

### <a name="picture"></a>Picture

Essas são propriedades comuns a imagens. Para limitar a pesquisa somente a imagens, a sintaxe é:

`kind:picture <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade     | Uso         | Exemplo               |
|--------------|-------------|-----------------------|
| Make da câmera  | cameramake  | cameramake:sample     |
| Modelo de câmera | cameramodel | cameramodel:sample    |
| Dimensões   | dimensions  | dimensões:8X10       |
| Orientation  | orientation | orientation:landscape |
| Data de tomada   | datetaken   | datetaken:ontem   |
| Largura        | width       | width:1600            |
| Altura       | altura      | height:1200           |



 

### <a name="video"></a>Vídeo

Essas são propriedades comuns a vídeos. Para limitar a pesquisa somente a vídeos, a sintaxe é:

`kind:video <property>:<value>`

em `<property>` que é uma propriedade listada abaixo e é o termo de pesquisa especificado pelo `<value>` usuário.



| Propriedade | Uso           | Exemplo                                |
|----------|---------------|----------------------------------------|
| Nome     | name, subject | name:"Family Vacation to the Beach 05" |
| Ramal      | ext, fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Tipos percebidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Chamando o WDS da linha de comando](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





