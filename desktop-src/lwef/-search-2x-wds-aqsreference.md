---
title: Sintaxe de consulta avançada
description: A sintaxe de consulta avançada (AQS) é usada pelo Microsoft Windows Desktop Search (WDS) para ajudar os usuários e os programadores a definir e restringir melhor suas pesquisas.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: bd00821e60c8d950a7ec384b62d7ff062066f224
ms.sourcegitcommit: 8bba855bfee06d018edb16c1af70fa4d4344445b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "105761222"
---
# <a name="advanced-query-syntax"></a>Sintaxe de consulta avançada

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

A sintaxe de consulta avançada (AQS) é usada pelo Microsoft Windows Desktop Search (WDS) para ajudar os usuários e os programadores a definir e restringir melhor suas pesquisas. Usar o AQS é uma maneira fácil de restringir as pesquisas e fornecer melhores conjuntos de resultados. As pesquisas podem ser limitadas pelos seguintes parâmetros:

-   Tipos de arquivo: pastas, documentos, apresentações, imagens e assim por diante.
-   Armazenamentos de arquivos: bancos de dados e locais específicos.
-   Propriedades do arquivo: tamanho, data, título e assim por diante.
-   Conteúdo do arquivo: palavras-chave como "resultados finais do projeto", "AQS", "Suede azul" e assim por diante.

Além disso, os parâmetros de pesquisa podem ser combinados usando operadores de pesquisa. O restante desta seção explica a sintaxe de consulta, os parâmetros e os operadores e como eles podem ser combinados para oferecer resultados de pesquisa direcionados. As tabelas descrevem a sintaxe a ser usada com o WDS, bem como as propriedades que podem ser consultadas para cada tipo de arquivo exibido na janela de resultados do **Windows Desktop Search** .

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

Os usuários podem limitar o escopo de suas pesquisas a locais de pasta ou armazenamentos de dados específicos. Por exemplo, se você usar várias contas de email e quiser limitar uma consulta ao Microsoft Outlook ou ao Microsoft Outlook Express, poderá usar `store:outlook` ou `store:oe` respectivamente.



| Restringir pesquisa por repositório de dados | Uso              | Exemplo                                  |
|-------------------------------|------------------|------------------------------------------|
| Área de trabalho                       | área de trabalho          | loja: área de trabalho                            |
| Arquivos                         | files            | armazenar: arquivos                              |
| Outlook                       | outlook          | loja: Outlook                            |
| Outlook Express               | OE               | Store: OE                                 |
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
| Documentos de texto                  | text             | tipo: texto                      |
| Planilhas                    | planilhas     | tipo: planilhas              |
| Apresentações                   | apresentações    | tipo: apresentações             |
| Música                           | music            | tipo: música                     |
| Imagens                        | classificação pics             | tipo: imgs                      |
| Vídeos                          | Vídeos           | tipo: vídeos                    |
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

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade       | Uso                      | Exemplo                        |
|----------------|--------------------------|--------------------------------|
| Título          | título, assunto ou sobre  | Título: "trimestral financeiro"    |
| Status         | status                   | status: concluído                |
| Data           | data                     | Data: última semana                 |
| Data da modificação  | DateModified ou modificado | modificado: última semana             |
| Importância     | importância ou prioridade   | importância: alta                |
| Tamanho           | tamanho                     | Tamanho: > 50                   |
| Excluído        | excluído ou isdeledo     | IsDeleted: true                 |
| É anexo  | isanexáment             | isanexáment: true              |
| Para             | para ou por nome             | para: Bob                         |
| Cc             | CC ou ccName             | CC: João                        |
| Empresa        | company                  | empresa: Microsoft              |
| Local       | local                 | local: "sala de conferências 102" |
| Categoria       | category                 | Categoria: negócios              |
| Palavras-chave       | palavras-chave                 | Palavras-chave: "projeções de vendas"   |
| Álbuns          | Álbuns                    | Álbum: "voar por noite"           |
| Nome do arquivo      | filename ou arquivo         | nome do arquivo: retomar              |
| Gênero          | gênero                    | Gênero: Rock                     |
| Autor         | autor ou por             | Autor: "Stephen King"          |
| Pessoas         | pessoas ou com           | com: (Sonja ou David)          |
| Pasta         | pasta, em ou caminho    | pasta: downloads               |
| Extensão de arquivo | ext ou fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Anexo

Essas são propriedades comuns a anexos. Para limitar a pesquisa a anexos somente, a sintaxe é:

`kind:attachment <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade | Uso            | Exemplo                  |
|----------|----------------|--------------------------|
| Pessoas   | pessoas ou com | pessoas: João ou com: João |



 

### <a name="contacts"></a>Contatos

Essas são propriedades comuns a contatos. Para limitar a pesquisa somente a contatos, a sintaxe é:

`kind:contacts <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade              | Uso                 | Exemplo                            |
|-----------------------|---------------------|------------------------------------|
| Cargo             | jobtitle            | JobTitle: CFO                       |
| Endereço de mensagens instantâneas            | imendereço           | imendereço: João\_doe@msn.com        |
| Telefone do assistente     | assistantsphone     | assistantsphone: 555-3323           |
| Nome do assistente        | Assistente       | AssistantName: Paul                 |
| Profession            | profissão          | Profissão: encanamento                 |
| Apelido              | apelido            | apelido: Tex                       |
| Cônjuge                | cônjuge              | cônjuge: Debbie                      |
| Cidade de negócios         | businesscity        | businesscity: Seattle               |
| Código postal comercial  | businesspostalcode  | businesspostalcode: 98006           |
| home page de negócios    | businesshomepage    | BusinessHomePage www. Microsoft. com |
| Número de telefone de retorno de chamada | callbackphonenumber | callbackphonenumber: 555-555-2121   |
| Telefone do carro             | Carphone            | Carphone: 555-555-2121              |
| Children              | menores de idade            | filhos: Timmy                     |
| Nome            | nome           | Nome: João                     |
| Sobrenome             | sobrenome            | sobrenome: Doe                       |
| Fax residencial              | homefax             | homefax: 555-555-2121               |
| Nome do gerente        | ManagerName        | ManagerName: João                  |
| Pager                 | pager               | pager: 555-555-2121                 |
| Telefone comercial        | ficha       | ficha: 555-555-2121         |
| Telefone residencial            | homePhone           | HomePhone: 555-555-2121             |
| Telefone celular          | MobilePhone         | MobilePhone: 555-555-2121           |
| Office                | Office              | Office: exemplo                      |
| Especiais           | especiais         | aniversário: 1/1/06                 |
| Birthday              | festa            | aniversário: 1/1/06                    |
| Página da Web              | página da web             | página da Web www. Microsoft. com          |



 

> [!Note]
>
> Os números de telefone são indexados como inseridos. Por exemplo, se um usuário não incluiu um código de país ou de área ao inserir o número de telefone, os usuários não poderão localizar um contato se estiver pesquisando com o código de país ou de área no número de telefone.

 

### <a name="communications"></a>Comunicações

Essas são propriedades comuns a comunicações. Para limitar a pesquisa somente a comunicações, a sintaxe é:

`kind:communications <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade       | Uso                           | Exemplo                         |
|----------------|-------------------------------|---------------------------------|
| De           | do ou do organizador             | de: João                       |
| Recebido       | recebido ou enviado              | enviado: ontem                  |
| Assunto        | assunto ou título              | Assunto: "trimestral financeiro"   |
| Tem anexo | HasAttachments, HasAttachment | HasAttachment: true              |
| Anexos    | anexos ou anexo     | attachment:presentation.ppt     |
| Cco            | Cco, bccname ou bccaddress    | BCC: Dave                        |
| Endereço CC     | ccaddress ou CC               | ccaddress: João\_doe@outlook.com |
| Sinalizador de acompanhamento | followupflag                  | followupflag: 2                  |
| Data de conclusão       | DueDate ou devido                | devido: última semana                   |
| Ler           | leitura ou IsRead                | é: leitura                         |
| Está concluído   | Membros IsCompleted                   | é: concluído                    |
| Incompleto     | incompleto ou IsComplete    | é: incompleto                   |
| Com sinalizador       | HasFlag ou issinalizado          | tem: sinalizador                        |
| Duration       | duration                      | Duração: > 50                |



 

### <a name="calendar"></a>Calendário

Essas são propriedades comuns a calendários. Para limitar a pesquisa somente a calendários, a sintaxe é:

`kind:calendar <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade  | Uso                      | Exemplo          |
|-----------|--------------------------|------------------|
| Recorrente | recorrente ou IsRecurring | é: recorrente     |
| Organizer | organizador, por ou de    | organizador: Debbie |



 

### <a name="documents"></a>Documentos

Essas são propriedades comuns a documentos. Para limitar a pesquisa somente a documentos, a sintaxe é:

`kind:documents <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade          | Uso             | Exemplo                       |
|-------------------|-----------------|-------------------------------|
| Comentários          | comments        | Comentários: "precisa de revisão final" |
| Salvo pela última vez por     | lastsavedby     | LASTSAVEDBY: João              |
| Gerenciador de documentos  | DocumentManager | DocumentManager: João          |
| Número de revisão   | revisionnumber  | RevisionNumber: 1.0.3          |
| Formato do documento   | DocumentFormat  | DocumentFormat: MIMETYPE       |
| Data da última impressão | datelastprinted | datelastprinted: última semana     |



 

### <a name="presentation"></a>Apresentação

Essas são propriedades comuns a apresentações. Para limitar a pesquisa apenas a apresentações, a sintaxe é:

`kind:presentation <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade    | Uso        | Exemplo           |
|-------------|------------|-------------------|
| Contagem de slides | slidecount | slidecount: >20 |



 

### <a name="music"></a>Música

Essas são propriedades comuns a arquivos de música. Para limitar a pesquisa apenas a músicas, a sintaxe é:

`kind:music <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade | Uso                | Exemplo                  |
|----------|--------------------|--------------------------|
| Taxa de bits | taxa de bits, Tarifa      | taxa de bits: 192              |
| Autor   | artista, por ou de | Artista: John cantor       |
| Duration | duration           | Duração: 3               |
| Álbuns    | Álbuns              | Álbum: "melhores acertos"    |
| Gênero    | gênero              | Gênero: Rock               |
| Rastrear    | rastrear              | faixa: 12                 |
| Year     | ano               | ano: > 1980 < 1990 |



 

### <a name="picture"></a>Picture

Essas são propriedades comuns a imagens. Para limitar a pesquisa apenas a imagens, a sintaxe é:

`kind:picture <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade     | Uso         | Exemplo               |
|--------------|-------------|-----------------------|
| Marca da câmera  | cameramake  | cameramake: exemplo     |
| Modelo de câmera | cameramodel | CameraModel: exemplo    |
| Dimensões   | dimensions  | Dimensões: 8X10       |
| Orientation  | orientation | orientação: paisagem |
| Data de início   | datetaken   | Datetaken: ontem   |
| Largura        | width       | largura: 1600            |
| Altura       | altura      | altura: 1200           |



 

### <a name="video"></a>Vídeo

Essas são propriedades comuns a vídeos. Para limitar a pesquisa apenas a vídeos, a sintaxe é:

`kind:video <property>:<value>`

em que `<property>` é uma propriedade listada abaixo e `<value>` é o termo de pesquisa especificado pelo usuário.



| Propriedade | Uso           | Exemplo                                |
|----------|---------------|----------------------------------------|
| Nome     | nome, assunto | Nome: "férias da família para a praia 05" |
| Ramal      | ext, fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Tipos observados](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Esquematable](-search-2x-wds-schematable.md)
</dt> <dt>

[Chamando o WDS por meio da linha de comando](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





