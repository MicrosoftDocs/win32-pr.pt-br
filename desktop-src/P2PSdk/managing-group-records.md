---
description: Um registro de grupo são dados específicos publicados em todos os membros ativos de um grupo de pares, por exemplo, uma mensagem de chat ou uma atualização de status específica do aplicativo.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Gerenciando registros de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2d0ba77a315043e638ddaa28615cf84654852a13e73347ee36ee4c7d66a6e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061394"
---
# <a name="managing-group-records"></a>Gerenciando registros de grupo

Um registro de grupo são dados específicos publicados em todos os membros ativos de um grupo de pares, por exemplo, uma mensagem de chat ou uma atualização de status específica do aplicativo. Um registro é representado pela estrutura [**de \_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) e contém as seguintes informações sobre um par:

-   A ID do registro é um valor que identifica exclusivamente um registro no grupo par.
-   Um GUID que especifica o tipo de registro. Os aplicativos podem dar suporte a diferentes tipos de registro. Um aplicativo interpreta o campo de **dados** de um registro com base no tipo de registro. Alguns GUIDs são reservados e a chamada à API retorna o **par \_ E não é \_ \_ autorizado** quando o aplicativo tenta usá-los.
-   Um conjunto de atributos de registro descritos como uma cadeia de caracteres XML. Os atributos são usados durante a pesquisa de registros. Para obter mais informações sobre atributos, consulte [gravar o esquema de atributo](record-attribute-schema.md).
-   A hora do ponto em que um registro é criado.
-   A hora do ponto em que um registro expira.
-   A hora do ponto em que um registro é modificado.
-   O criador de um registro.
-   O membro que modifica um registro.
-   Uma estrutura de [**\_ dados de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_data) que contém a assinatura criptográfica para todos os campos nesta estrutura de [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Este campo não pode ser atualizado ou alterado diretamente por um par.
-   Uma estrutura de [**\_ dados de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_data) que contém os dados específicos do aplicativo associados a esse registro como uma matriz de bytes. O tipo de dados presente nesse campo é determinado pelo tipo de registro definido pelo aplicativo.

## <a name="obtaining-peer-group-records"></a>Obtendo registros de grupo de pares

Registros individuais são obtidos chamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) com a ID do registro. Ao processar todos os registros de um tipo específico, o conjunto enumerado de todos os registros de grupo de pares atuais é obtido primeiro chamando [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) para abrir a enumeração e, em seguida, chamando iterativamente [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) até que todos os registros sejam recuperados. Quando terminar, feche a enumeração e libere a memória associada a ela chamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

Quando um registro é criado, excluído ou atualizado por um par, o registro afetado é publicado em todos os membros do grupo de pontos por meio do evento **de \_ \_ alteração de \_ registro \_ de evento do grupo de pares** . Observe que, se um par não estiver conectado ao grupo, ele receberá o registro atualizado e, na próxima vez que se conectar. É importante se registrar para esse evento com [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) se seu aplicativo mantiver ou gerenciar registros de forma significativa. Como alternativa, o aplicativo pode consultar o banco de dados de registro sob demanda usando [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords).

Quando o evento de alteração de registro de evento de grupo de pares é gerado, a ID e o tipo de registro específicos, bem como o tipo de alteração (adicionar, atualizar, excluir) é recebido como uma estrutura de [**dados de alteração de registro de evento de pares \_ \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) . **\_ \_ \_ \_** Essa estrutura é obtida com uma chamada para [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Se a alteração for uma adição ou uma atualização, você deverá usar [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) para obter o registro com a ID fornecida. O banco de dados de registro local para a infraestrutura é atualizado automaticamente.

Você também pode pesquisar registros específicos com base em atributos personalizados específicos fornecidos no campo **pwzAttributes** do [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record), bem como quaisquer atributos predefinidos. Para fazer isso, use a função [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) com uma consulta de pesquisa XML formatada conforme especificado no tópico [formato de consulta de pesquisa de registro](record-search-query-format.md) .

Para obter mais detalhes sobre como trabalhar com registros na infraestrutura par, consulte o tópico [registros](records.md) em [usando a infraestrutura de pares](using-the-peer-infrastructure.md).

## <a name="administration-of-peer-group-records"></a>Administração de registros de grupo de pares

Quando os convites iniciais são emitidos pelo criador do grupo de pares, ele pode especificar que determinados membros sirvam em uma função administrativa (administrador da função de grupo de pares \_ \_ \_ ) sempre que emitir novas credenciais para o usuário (por meio de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) ou [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)). Um administrador tem a capacidade de adicionar, excluir e atualizar diretamente qualquer registro de grupo de mesmo nível. Por outro lado, um membro do grupo de pares com sua função definida como membro da **\_ \_ função \_ de grupo par** ou **função de grupo par \_ \_ \_ convidando \_ membro** só pode adicionar, atualizar e excluir seus próprios registros.

O criador tem a função de administrador por padrão.

Para atualizar um registro, obtenha o registro com [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) ou [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords), faça as alterações e passe o registro atualizado para [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord).

Para excluir um registro, passe a ID do registro para excluir para [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord).

Para adicionar um registro, crie uma nova estrutura de [**\_ registro de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_record) e preencha os seguintes campos:

-   **dwSize**. Este campo contém o valor de **sizeof**([**\_ registro par**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftExpiration**. Este campo contém a data e a hora de expiração deste registro, expressos em tempo de emparelhamento como uma estrutura **FILETIME** .
-   **digite**. Este campo contém um valor de **GUID** que identifica o tipo de registro para o aplicativo. Se esse tipo for personalizado para sua infraestrutura de aplicativo, você também deverá preencher o campo de **dados** .

Os campos a seguir são preenchidos pela infraestrutura do e serão ignorados se forem definidos pelo aplicativo:

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

Os campos restantes são opcionais. Para adicionar esse novo registro ao grupo par, passe-o para [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord).

## <a name="importing-and-exporting-records"></a>Importando e exportando registros

Os registros de grupo ponto a ponto são mantidos localmente como um banco de dados. Para salvar um instantâneo atual do banco de dados de registro de grupo par em um arquivo local, chame [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)e passe-o para o grupo par. Esse arquivo pode ser transportado para um computador ou aplicativo diferente, que pode extrair e usar esse banco de dados de registro chamando [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase).

 

 



