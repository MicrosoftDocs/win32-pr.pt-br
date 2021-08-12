---
description: Este tópico discute o processo de convidar um par para ingressar em um grupo de pares usando as APIs de agrupamento de pares.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Convidando um par a um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760c2fb6023d5332da74402726669367fee4f5102c99269fa8e603653a1e2eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612646"
---
# <a name="inviting-a-peer-to-a-group"></a>Convidando um par a um grupo

Este tópico discute o processo de convidar um par para ingressar em um grupo de pares usando as APIs de agrupamento de pares.

Um grupo de pares requer credenciais válidas para participar. As credenciais são emitidas de fora de um grupo na forma de convites ou diretamente aos membros de um grupo quando são necessárias atualizações de credenciais.

## <a name="group-member-certificates"></a>Certificados de membro de grupo

Um grupo de pares é criado quando um aplicativo faz uma chamada para [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).

Para participar de um grupo de pares, cada par deve ter uma identidade de par. Chame [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) até que todas as identidades de pares definidas para o par tenham sido retornadas e selecione aquela que deve ser usada. Se uma identidade de par não existir, crie uma chamando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

Cada identidade de par é associada a um conjunto específico de credenciais que podem ser usadas para provar a associação de grupo de sistemas pares ao se conectar, bem como ao publicar registros ou convidar membros adicionais. Essas credenciais são representadas como cadeias de [certificados X. 509](https://www.ietf.org/rfc/rfc2511.txt) chamados de GMC (certificados de associação de grupo).

Para criar o GMC para uma identidade de par, você deve primeiro obter sua chave pública. Essa chave é obtida chamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) no possível convidado e passando sua identidade de par. Essa função retorna um certificado codificado em base 64 (IDC) que contém a chave pública RSA usada para criar o GMC para a identidade de par (entre outras coisas), encapsulada em um blob XML, no seguinte formato:

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Essa cadeia de caracteres pode ser passada para [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), que retorna um convite que contém o GMC para essa identidade de par. O convite deve ser passado para o convidado usando um processo diferente, como email, FTP ou um compartilhamento de arquivos seguro.

Como alternativa, a própria IDC pode ser colocada em uma nova estrutura de [**\_ \_ informações de credenciais de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) e transmitida para [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials), que, da mesma forma, gera um convite.

Observe que os aplicativos não têm permissão para adicionar marcas na marca **PEERIDENTITYINFO** ou modificar esse fragmento XML de qualquer forma. Os aplicativos têm permissão para incorporar esse fragmento XML em outros documentos XML, mas devem retirar todo o XML específico do aplicativo antes de passar esse fragmento para as funções [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) ou [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) .

Os GMCs de membros são emitidos por administradores e pelo criador do grupo de pares. Os membros devem obter novos GMCs com tempos de vida estendidos seus GMCs antes que o tempo de expiração tenha passado. O administrador do grupo de sistemas pares emite credenciais atualizadas chamando [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) com as credenciais existentes para esse par.

A estrutura de [**\_ \_ informações de credenciais de par**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) contém os dados básicos do status de associação de um par, incluindo a chave pública para seus GMC. As credenciais emitidas recentemente podem ser publicadas no grupo de pares definindo o \_ sinalizador de credenciais do repositório do grupo par \_ \_ na chamada para [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Quando o destinatário das novas credenciais ingressar no grupo par, as credenciais existentes serão atualizadas pela infraestrutura de agrupamento de pares.

## <a name="issuing-an-invitation"></a>Emitindo um convite

Um membro é convidado para ingressar no grupo de pares de uma das duas maneiras a seguir:

-   Um administrador de grupo de sistemas pares chama [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), passando a cadeia de caracteres XML de informações de identidade obtida do convidado potencial por meio de um mecanismo comum fora de banda, como email ou uma sessão de mensagem instantânea. O convite também é transmitido por algum processo ou mecanismo externo para o par, que, por fim, o receberá como uma cadeia de caracteres XML ou um arquivo de texto.
-   Um administrador de grupo de sistemas pares chama [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Para usar essa função, o par deve já ter publicado informações de associação para o grupo par [**( \_ membro par**](/windows/desktop/api/P2P/ns-p2p-peer_member)) ou ter uma chave pública disponível (do par de chaves RSA usado para criar a identidade da entidade). No primeiro caso, a estrutura [**de \_ \_ informações de credenciais de par**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) necessária para **PeerGroupIssueCredentials** pode ser obtida na estrutura de **\_ membros de pares** ; no último caso, uma nova estrutura de **\_ \_ informações de credenciais de par** pode ser populada com a chave pública.

Depois de receber a cadeia de caracteres de convite, o ponto passa a ela para [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) para ingressar no grupo de pares. Se a chamada para **PeerGroupJoin** for bem-sucedida, o par poderá abrir o grupo de par mais tarde chamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen).

## <a name="parsing-an-invitation"></a>Analisando um convite

Opcionalmente, um convite pode ser analisado chamando [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation), que retorna uma estrutura [**de \_ \_ informações de convite de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) . Os campos na estrutura podem ser facilmente obtidos para fins de exibição.

 

 



