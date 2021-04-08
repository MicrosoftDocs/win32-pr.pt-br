---
description: Conforme mencionado anteriormente, a função WSAJoinLeaf é usada para ingressar um nó folha em uma sessão do MultiPoint.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Usando WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027262a117edc5541a4809481aa4607837343b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828670"
---
# <a name="using-wsajoinleaf"></a>Usando WSAJoinLeaf

Conforme mencionado anteriormente, a função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) é usada para ingressar um nó folha em uma sessão do MultiPoint. **WSAJoinLeaf** tem os mesmos parâmetros e semântica que [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) , exceto pelo fato de que ele retorna um descritor de soquete (como em [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) e tem um parâmetro *dwFlags* adicional.

O parâmetro *dwFlags* é usado para indicar se o soquete estará agindo somente como um remetente, somente como um receptor ou ambos. Somente os soquetes do MultiPoint podem ser usados para os parâmetros de entrada *s* nesta função. Se o soquete do MultiPoint estiver no modo de não bloqueio, o descritor de soquete retornado não será utilizável até que uma indicação de conexão FD correspondente \_ seja recebida. Um aplicativo raiz em uma sessão do MultiPoint pode chamar [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) uma ou mais vezes para adicionar um número de nós folha, no entanto, no máximo uma solicitação de conexão do MultiPoint pode estar pendente por vez.

O descritor de soquete retornado por [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) difere dependendo se o descritor de soquete de entrada, *s*, é uma \_ raiz c ou uma \_ folha c. Quando usado com um \_ soquete raiz c, o parâmetro *Name* designa um nó folha específico a ser adicionado e o descritor de soquete retornado é um \_ soquete folha c correspondente ao nó folha recém-adicionado. Ele não se destina a ser usado para a troca de dados do MultiPoint, mas sim é usado para receber indicações do FD \_ xxx (por exemplo, FD \_ Close) para a conexão que existe para a folha c específica \_ . Algumas implementações do MultiPoint também podem permitir que esse soquete seja usado para chats colaterais entre a raiz e um nó folha individual. Uma \_ indicação de fechamento FD será recebida para este Soquete se o nó folha correspondente chamar [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) para sair da sessão do MultiPoint. Simetricamente, invocar **fechamento** no \_ soquete folha c retornado de **WSAJoinLeaf** faz com que o soquete no nó folha correspondente obtenha uma \_ notificação FD Close.

Quando [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) é invocado com um \_ soquete de folha c, o parâmetro Name contém o endereço do aplicativo raiz (para um esquema de controle com raiz) ou uma sessão de MultiPoint existente (esquema de controle *sem* raiz) e o descritor de soquete retornado é o mesmo que o descritor de soquete de entrada. Em um esquema de controle com raiz, o aplicativo raiz coloca seu \_ soquete raiz c no modo de escuta chamando [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen). A notificação de aceitação padrão do FD \_ é entregue quando o nó folha solicita a associação a si mesma à sessão do MultiPoint. O aplicativo raiz usa as funções [](/windows/desktop/api/Winsock2/nf-winsock2-accept) / [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) de aceitação usuais para admitir o novo nó folha. O valor retornado de **Accept** ou **WSAAccept** também é um \_ descritor de soquete folha c, assim como os retornados de **WSAJoinLeaf**. Para acomodar os esquemas do MultiPoint que permitem junções iniciadas pela raiz e por folha, é aceitável \_ que um soquete raiz c que já esteja no modo de escuta seja usado como entrada para **WSAJoinLeaf**.

Um aplicativo raiz do MultiPoint é geralmente responsável pelo Dismantling ordenado de uma sessão do MultiPoint. Esse aplicativo pode usar [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) ou [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) em um \_ soquete raiz c para causar todos os \_ soquetes de folha c associados, incluindo aqueles retornados de [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) e seus \_ soquetes de folha c correspondentes nos nós folha remota, para obter \_ notificação de fechamento de FD.

 

 



