---
description: Conforme mencionado anteriormente, a função WSAJoinLeaf é usada para unir um nó folha em uma sessão de vários pontos.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Usando WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13b6d82960f74135fa519a1284a1274b878e18c32f59d9c2b8c46ebd592c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121016"
---
# <a name="using-wsajoinleaf"></a>Usando WSAJoinLeaf

Conforme mencionado anteriormente, a [**função WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) é usada para unir um nó folha em uma sessão de vários pontos. **O WSAJoinLeaf** tem os mesmos parâmetros e semântica que [**WSAConnect,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) exceto que ele retorna um descritor de soquete (como no [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) e tem um parâmetro *dwFlags adicional.*

O *parâmetro dwFlags* é usado para indicar se o soquete atuará apenas como um remetente, apenas como um receptor ou ambos. Somente soquetes de vários pontos podem ser usados para os *parâmetros de entrada* nesta função. Se o soquete de vários pontos estiver no modo de não desbloqueio, o descritor de soquete retornado não será acessível até que uma indicação correspondente do FD \_ CONNECT seja recebida. Um aplicativo raiz em uma sessão multiponto pode chamar [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) uma ou mais vezes para adicionar vários nós folha, no entanto, no máximo uma solicitação de conexão multipoint pode estar pendente por vez.

O descritor de soquete retornado por [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) difere dependendo se o descritor de soquete de entrada, *s*, é uma raiz c ou \_ uma folha \_ c. Quando usado com um soquete raiz c, o parâmetro name designa um nó folha específico a ser adicionado e o descritor de soquete retornado é um soquete folha c correspondente ao nó folha \_  \_ recém-adicionado. Ele não se destina a ser usado para a troca de dados de vários pontos, mas sim para receber indicações de FD \_ XXX (por exemplo, FD CLOSE) para a conexão que existe com a folha \_ c \_ específica. Algumas implementações de vários pontos também podem permitir que esse soquete seja usado para chats laterais entre a raiz e um nó folha individual. Uma indicação FD CLOSE será recebida para esse soquete se o nó folha correspondente chamar \_ [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) para sair da sessão de vários pontos. Simetricamente, invocar **closesocket** no soquete folha c retornado de \_ **WSAJoinLeaf** faz com que o soquete no nó folha correspondente receba uma notificação FD \_ CLOSE.

Quando [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) é invocado com um soquete folha c, o parâmetro name contém o endereço do aplicativo raiz (para um esquema de controle com raiz) ou uma sessão multipoint existente (esquema de controle não controlado) e o descritor de soquete retornado é o mesmo que o descritor de soquete \_ de entrada.  Em um esquema de controle com raiz, o aplicativo raiz coloca seu soquete raiz C no modo de \_ escuta chamando [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen). A notificação PADRÃO DE ACEITAÇÃO do FD é entregue quando o nó folha solicita para \_ ingressar na sessão de vários pontos. O aplicativo raiz [](/windows/desktop/api/Winsock2/nf-winsock2-accept)usa as funções / [**comuns de aceitação WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) para reconhecer o novo nó folha. O valor retornado de **accept** ou **WSAAccept** também é um descritor de soquete folha c, assim como aqueles retornados \_ de **WSAJoinLeaf.** Para acomodar esquemas de vários pontos que permitem junções iniciadas por raiz e iniciadas por folha, é aceitável que um soquete raiz C que já está no modo de escuta seja usado como entrada para \_ **WSAJoinLeaf.**

Um aplicativo raiz multiponto geralmente é responsável pela desataramento de uma sessão de vários pontos. Esse aplicativo pode [](/windows/desktop/api/winsock/nf-winsock-shutdown) usar shutdown ou [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) em um soquete raiz c para fazer com que todos os soquetes folha c associados, incluindo aqueles retornados de \_ \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) e seus soquetes folha C correspondentes nos nós folha remotos, para obter notificação \_ FD \_ CLOSE.

 

 



