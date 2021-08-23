---
description: O multicast de IP se enquadra na categoria de plano de dados não-raiz e plano de controle não raiz.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: Multicast de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b80441826f490fedc3dac3dba405ddd0d9f09d57bfd0243a66cae320c76b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051494"
---
# <a name="ip-multicast"></a>Multicast de IP

O multicast de IP se enquadra na categoria de plano de dados não-raiz e plano de controle não raiz. Todos os aplicativos desempenham uma função de folha. Atualmente, a maioria das implementações de multicast de IP usa um conjunto de opções de soquete propostas por Steve Deering para a IETF (Internet Engineering Task Force). Cinco operações são, portanto, disponibilizadas:

-   \_ \_ TTL de multicast de IP – define o escopo de vida de controles de uma sessão de multicast.
-   IP \_ multicast \_ If — determina a interface a ser usada para multicast.
-   IP \_ Add \_ MEMBERSHI – une uma sessão de multicast especificada.
-   \_ \_ Associação de IP drop — sai de uma sessão multicast.
-   \_Loop multicast \_ de IP — controla o loopback do tráfego multicast.

Definir a vida útil para um soquete de multicast de IP mapeia diretamente para o uso do código de \_ comando de escopo multicast sio \_ para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).

o método para determinar a interface IP a ser usada para multicast é por meio de uma opção de soquete específica de TCP/IP, conforme descrito no Windows sockets 2 Protocol-Specific anexo. as três operações restantes são bem cobertas com a semântica do Windows sockets 2 descrita aqui.

O aplicativo abriria soquetes com \_ sinalizadores folha c/d \_ em [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Ele usaria [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para se adicionar a um grupo de multicast na interface padrão designada para operações de multicast. Se o sinalizador em **WSAJoinLeaf** indicar que esse soquete é apenas um remetente, a operação de junção será essencialmente uma não operacional e nenhuma mensagem IGMP precisará ser enviada. Caso contrário, um pacote IGMP é enviado para o roteador para indicar os interesses no recebimento de pacotes enviados para o endereço de multicast especificado. Como o aplicativo criou \_ soquetes de folha c folha/d especiais \_ usados apenas para executar multicast, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) padrão seria usada para sair da sessão de multicast. O \_ código de \_ comando de auto-retorno do sio MultiPoint para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) fornece um mecanismo de controle genérico para determinar se os dados enviados em um \_ soquete de folha d em um esquema MultiPoint não raiz também podem ser recebidos no mesmo soquete.

> [!Note]  
> a versão do Winsock da \_ opção de loop multicast de ip \_ é semanticamente diferente da versão UNIX da \_ opção de loop multicast de ip \_ :

 

-   No Winsock, a \_ opção de \_ loop multicast IP se aplica somente ao caminho de recebimento.
-   na versão UNIX, a opção de \_ LOOP MULTICAST IP \_ se aplica ao caminho de envio.

Por exemplo, aplicativos ATIVAdos e desativados (que são mais fáceis de rastrear que X e Y) ingressam no mesmo grupo na mesma interface; aplicativo em define a \_ opção de \_ loop multicast IP on, Application off define a \_ opção de loop multicast IP como \_ off. Se ON e OFF são aplicativos Winsock, OFF pode enviar para ON, mas ON não pode ser enviado para OFF. por outro lado, se ON e off forem UNIX aplicativos, on poderá enviar para OFF, mas OFF não pode enviar para ON.

 

 



