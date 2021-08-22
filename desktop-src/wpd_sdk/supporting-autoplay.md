---
description: Suporte à reprodução automática
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Suporte à reprodução automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83091191d8468b7ea3d34146e4a4c02e8cf5bf80cb3e49c72dc43bb092d10f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083390"
---
# <a name="supporting-autoplay"></a>Suporte à reprodução automática

A reprodução automática é um recurso do shell que inicia os aplicativos associados a determinados dispositivos. Dependendo das configurações atuais de reprodução automática, esse recurso executará uma das várias ações, como apresentar uma lista de aplicativos de manipulador disponíveis, exibindo uma exibição de pasta padrão de arquivos e assim por diante.

no Windows Vista, o recurso de reprodução automática foi estendido para que um dispositivo WPD possa fornecer uma lista de tipos de conteúdo que ele suporta. Da mesma forma, os aplicativos WPD podem registrar tipos de conteúdo para os quais dão suporte. Por exemplo, um assistente de aquisição de fotos pode ser registrado como um manipulador para qualquer dispositivo WPD que fornece imagens, e um aplicativo multimídia pode se registrar como um manipulador para qualquer dispositivo que armazene arquivos de áudio ou de vídeo.

os aplicativos registram informações específicas do manipulador escrevendo entradas para o **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer AutoplayHandlers de \\ \\ manipuladores** de chave. Usando um manipulador de aplicativo WPD (chamado MyWpdApplication.exe) como exemplo, o aplicativo pode inserir os seguintes valores em uma chave **\\ \\ MyWpdApplicationHandler de manipuladores** .



| Valor          | Tipo            | Dados                                                 |
|----------------|-----------------|------------------------------------------------------|
| Ação         | REG \_ sz         | Procurar conteúdo em dispositivos portáteis.                  |
| CLSIDForCancel | REG \_ sz         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ expande \_ sz | % SystemDrive% \\ multimídia \\ WPD \\MyWpdApplication.exe |
| InitCmdLine    | REG \_ sz         | /AutoPlay                                            |
| ProgID         | REG \_ sz         | MyWpdApplication.MyWpdApplicationAutoPlay            |
| Provedor       | REG \_ sz         | MyWpdApplication                                     |



 

para obter mais informações sobre as chaves e os valores do registro de reprodução automática encontrados na chave **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ handlers** , consulte a documentação correspondente no MSDN.

### <a name="the-wpd-autoplay-scheme"></a>O esquema de reprodução automática WPD

o esquema de reprodução automática WPD integra-se com o recurso de reprodução automática do Windows Vista. Ele faz isso dando suporte a três categorias de reprodução automática, que são descritas na tabela a seguir.



| Categoria | Descrição                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| Fonte   | Um dispositivo WPD pode ser tratado como uma fonte de conteúdo (ou seja, o conteúdo pode ser transferido do dispositivo).        |
| Coletor     | Um dispositivo WPD pode ser tratado como um destino para o conteúdo (ou seja, o conteúdo pode ser transferido para o dispositivo).    |
| Função | Um dispositivo WPD dá suporte a um recurso programável ou controlável (por exemplo, ele pode enviar e receber mensagens SMS). |



 

Os aplicativos se registram para as categorias de origem, coletor e/ou função apropriadas, gravando entradas na seção de reprodução automática do registro do sistema. essas entradas aparecem na chave **HKEY \_ LOCAL \_ \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ eventhandlers \\ WPD** key. A chave WPD é a **função**, o **coletor** e as chaves de **origem** . Em cada uma dessas chaves é um GUID que corresponde a uma categoria funcional WPD ou tipo de conteúdo.

A tabela a seguir lista os GUIDs encontrados na chave de **função** no registro e identifica a categoria funcional que corresponde a cada GUID.



| Categoria funcional WPD                           | Chave do registro (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| \_toda a \_ categoria \_ funcional WPD                    | {2D8A6512-A74C-448E-BA8A-F4AC07C49399} |
| \_captura de \_ áudio de categoria funcional \_ WPD \_         | {3F2A1919-C7C2-4A00-855D-F57CF06DEBBB} |
| \_dispositivo de \_ categoria \_ funcional WPD                 | {08EA466B-E3A4-4336-A1F3-A44D2B5C438C} |
| \_configuração de \_ rede de categoria funcional \_ WPD \_ | {48F4DB72-7C6A-4AB0-9E1A-470E3CDBF26A} |
| \_informações de \_ renderização de categoria funcional \_ WPD \_ | {08600BA4-A7BA-4A01-AB0E-0065D0A356D3} |
| \_categoria funcional \_ WPD \_ SMS                    | {0044A0B1-C1E9-4AFD-B358-A62C6117C9CF} |
| a \_ categoria funcional WPD \_ \_ ainda \_ captura de imagem \_  | {613CA327-AB93-4900-B4FA-895BB5874B79} |
| \_armazenamento de \_ categoria \_ funcional WPD                | {23F05BBC-15DE-4C2A-A55B-A9AF5CE412EF} |
| \_captura de \_ vídeo de categoria funcional \_ WPD \_         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

A tabela a seguir lista os GUIDs encontrados no **coletor** e as chaves de **origem** no registro e identifica o tipo de conteúdo que corresponde a cada GUID.



| Tipo de conteúdo WPD                          | Chave do registro (GUID)                    |
|-------------------------------------------|----------------------------------------|
| \_ \_ todos os tipos de conteúdo WPD \_                   | {80E170D2-1055-4A3E-B952-82CC4F8A8689} |
| \_compromisso de \_ tipo de conteúdo WPD \_           | {0FED060E-8793-4B1E-90C9-48AC389AC631} |
| \_áudio de \_ tipo de conteúdo WPD \_                 | {4AD2C85E-5E2D-45E5-8864-4F229E3C6CF0} |
| \_álbum de \_ áudio do tipo de conteúdo WPD \_ \_          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| \_calendário de \_ tipo de conteúdo WPD \_              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| \_certificado de \_ tipo de conteúdo WPD \_           | {DC3876E8-A948-4060-9050-CBD77E8A3D87} |
| \_contato de \_ tipo de conteúdo WPD \_               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| \_grupo de \_ contatos de tipo de conteúdo WPD \_ \_        | {346B8932-4C36-40D8-9415-1828291F9DE9} |
| \_documento de \_ tipo de conteúdo WPD \_              | {680ADF52-950A-4041-9B41-65E393648155} |
| \_email de \_ tipo de conteúdo WPD \_                 | {8038044A-7E51-4F8F-883D-1D0623D14533} |
| \_pasta de \_ tipo de conteúdo WPD \_                | {27E2E392-A111-48E0-AB0C-E17705A05F85} |
| \_ \_ objeto funcional de tipo de conteúdo WPD \_ \_    | {99ED0160-17FF-4C44-9D98-1D7A6F941921} |
| \_ \_ arquivo genérico de tipo de conteúdo WPD \_ \_         | {0085E0A6-8D34-45D7-BC5C-447E59C73D48} |
| \_ \_ mensagem genérica do tipo de conteúdo WPD \_ \_      | {E80EAAF8-B2DB-4133-B67E-1BEF4B4A6E5F} |
| \_imagem de \_ tipo de conteúdo WPD \_                 | {EF2107D5-A52A-4243-A26B-62D4176D7603} |
| WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM          | {75793148-15F5-4A30-A813-54ED8A37E226} |
| CAST DE MÍDIA \_ DO \_ TIPO DE \_ CONTEÚDO \_ WPD           | {5E88B3CC-3E65-4E62-BFFF-229495253AB0} |
| MEMO DE \_ TIPO \_ DE CONTEÚDO \_ WPD                  | {9CD20ECF-3B50-414F-A641-E473FFE45751} |
| WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM | {00F0C3AC-A593-49AC-9219-24ABCA5A2563} |
| ASSOCIAÇÃO DE REDE DO \_ \_ TIPO DE CONTEÚDO \_ WPD \_  | {031DA7EE-18C8-4205-847E-89A11261D0F3} |
| PLAYLIST DO TIPO DE CONTEÚDO WPD \_ \_ \_              | {1A33F7E4-AF13-48F5-994E-77369DFE04A3} |
| PROGRAMA DE TIPO \_ DE \_ CONTEÚDO \_ WPD               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| SEÇÃO TIPO DE \_ \_ CONTEÚDO \_ WPD               | {821089F5-1D91-4DC9-BE3C-BBB1B35B18CE} |
| TAREFA TIPO \_ DE \_ CONTEÚDO \_ WPD                  | {63252F2C-887F-4CB6-B1AC-D29855DCEF6C} |
| TV DO \_ TIPO DE \_ CONTEÚDO WPD \_            | {60A169CF-F2AE-4E21-9375-9677F11C1C6E} |
| TIPO DE CONTEÚDO WPD \_ \_ NÃO \_ ESPECIFICADO           | {28D8D31E-249C-454E-AABC-34883168E634} |
| VÍDEO DO TIPO \_ \_ DE CONTEÚDO WPD \_                 | {9261B03C-3D78-4519-85E3-02C5E1F50BB9} |
| ÁLBUM DE VÍDEO \_ DO \_ TIPO DE CONTEÚDO \_ WPD \_          | {012B0DB7-D4C1-45D6-B081-94B87779614F} |
| PERFIL SEM FIO DO \_ \_ TIPO DE \_ \_ CONTEÚDO WPD     | {0BAC070A-9F5F-4DA4-A8F6-3DE44D68FD6C} |



 

Se um aplicativo tiver suporte para uma determinada função, origem ou categoria de sink, ele inserirá uma cadeia de caracteres especificando o nome da chave do manipulador no GUID que identificou a categoria funcional ou de tipo de conteúdo com suporte. Usando MyWpdApplication como exemplo, o aplicativo criaria uma entrada no ... **/EventHandlers/WPD/Function** ou **/Sink** ou **/Source** keys. Essa entrada teria o formato "MyWpdApplicationHandler" e ser do tipo REG \_ SZ. Além disso, essa entrada seria exibida sob o GUID para as categorias funcionais ou tipos de conteúdo aos quais o aplicativo dá suporte.

 

 



