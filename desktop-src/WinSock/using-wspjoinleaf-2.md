---
description: Como mencionado anteriormente, o WSPJoinLeaf é usado para unir um nó folha em uma sessão do MultiPoint.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Usando WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4426c0d22657b26dcc2217d856865d9ebe98db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164460"
---
# <a name="using-wspjoinleaf"></a>Usando WSPJoinLeaf

Como mencionado anteriormente, o [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) é usado para unir um nó folha em uma sessão do MultiPoint. **WSPJoinLeaf** tem os mesmos parâmetros e semântica que [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , exceto pelo fato de que ele retorna um descritor de soquete (como em [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)) e tem um parâmetro *dwFlags* adicional. O parâmetro *dwFlags* é usado para indicar se o soquete estará agindo somente como um remetente, somente como um receptor ou ambos. Somente os soquetes do MultiPoint podem ser usados para os parâmetros de entrada *s* nesta função. Se o soquete do MultiPoint estiver no modo de não bloqueio, o descritor de soquete retornado não será utilizável até que uma indicação de conexão FD correspondente \_ tenha sido recebida. Um aplicativo raiz em uma sessão do MultiPoint pode chamar **WSPJoinLeaf** uma ou mais vezes para adicionar um número de nós folha, no entanto, no máximo uma solicitação de conexão do MultiPoint pode estar pendente por vez.

O descritor de soquete retornado por [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) é diferente dependendo se o descritor de soquete de entrada, *s*, é uma \_ raiz c ou uma \_ folha c. Quando usado com um \_ soquete raiz c, o parâmetro *Name* designa um nó folha específico a ser adicionado e o descritor de soquete retornado é um \_ soquete folha c correspondente ao nó folha recém-adicionado. Ele não se destina a ser usado para a troca de dados do MultiPoint, mas é usado para receber indicações de eventos de rede (por exemplo, o uso de FD \_ Close) para a conexão que existe para a folha c em particular \_ . Algumas implementações do MultiPoint também podem permitir que esse soquete seja usado para chats colaterais entre a raiz e um nó folha individual. Uma \_ indicação de fechamento FD deve ser fornecida para este Soquete se o nó folha correspondente chamar [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) para sair da sessão do MultiPoint. Simetricamente, invocar **WSPCloseSocket** no \_ soquete folha c retornado de [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) fará com que o soquete no nó folha correspondente obtenha a notificação de \_ fechamento FD.

Quando [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) é invocado com um \_ soquete de folha c, o parâmetro Name contém o endereço do aplicativo raiz (para um esquema de controle com raiz) ou uma sessão de MultiPoint existente (esquema de controle *sem* raiz) e o descritor de soquete retornado é o mesmo que o descritor de soquete de entrada. Em um esquema de controle com raiz, o cliente raiz colocaria seu \_ soquete raiz c no modo de escuta chamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)). A notificação de aceitação do Standard FD \_ será entregue quando o nó folha solicitar a associação a si mesma à sessão do MultiPoint. O cliente raiz usa a função [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) usual para admitir o novo nó folha. O valor retornado de **WSPAccept** também é um \_ descritor de soquete folha c, assim como os retornados de **WSPJoinLeaf**. Para acomodar os esquemas do MultiPoint que permitem junções iniciadas pela raiz e por folha, é aceitável \_ que um soquete raiz c que já esteja no modo de escuta seja usado como entrada para **WSPJoinLeaf**.

Um cliente raiz do MultiPoint é geralmente responsável pelo Dismantling ordenado de uma sessão do MultiPoint. Esse aplicativo pode usar [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) ou [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) em um \_ soquete raiz c para fazer com que todos os \_ soquetes de folha c associados, incluindo aqueles retornados de [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) e seus \_ soquetes de folha c correspondentes nos nós folha remoto, obtenham uma \_ notificação de fechamento FD.

 

 
