---
description: com base na taxonomia definida para esquemas de multipoint/multicast independentes de protocolo do Windows sockets 2, o ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Detalhes da função ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b089d02653ee996acc249f63144654c952ba724425fb208d9eb35cc9c2589e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051374"
---
# <a name="winsock-atm-function-details"></a>Detalhes da função ATM do Winsock

com base na taxonomia definida para esquemas de multipoint/multicast independentes de protocolo do Windows sockets 2, o ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz. (consulte a especificação da API do Windows sockets 2, o apêndice D para obter mais informações.) Um aplicativo agindo como a raiz criará \_ soquetes raiz c, e as contrapartes em execução em nós folha utilizarão \_ soquetes de folha c. O aplicativo raiz usará [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para adicionar novos nós folha. Os aplicativos correspondentes nos nós folha terão definido seus \_ soquetes folha c no modo de escuta. **WSAJoinLeaf** com um \_ soquete raiz c especificado será mapeado para a mensagem de instalação do Q. 2931 (para a primeira folha) ou para adicionar a mensagem da parte (para qualquer uma das folhas subsequentes).

> [!Note]  
> Os parâmetros de QoS especificados em **WSAJoinLeaf** para quaisquer folhas subsequentes devem ser ignorados segundo a especificação uni do fórum ATM.

 

A junção iniciada por folha não faz parte do ATM UNI 3,1, mas tem suporte no ATM UNI 4,0. Portanto, o [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) com um \_ soquete folha c especificado pode ser mapeado para a mensagem ATM UNI 4,0 apropriada.

O parâmetro AAL e a negociação B-LLI têm suporte por meio da modificação das s correspondentes no parâmetro *lpSQOS* na invocação da função Condition especificada em [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).

> [!Note]  
> Somente determinados campos nessas duas s podem ser modificados. Consulte o Apêndice C e o Apêndice F da especificação UNI do ATM Forum para obter detalhes.

 

 

 



