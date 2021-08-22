---
description: O ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Ponto ATM para MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198d8160fdb1e942cc581374af18ca57303726bdddd41142855d366e58dfbf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504456"
---
# <a name="atm-point-to-multipoint"></a>Ponto ATM para MultiPoint

O ATM se enquadra na categoria de dados com raiz e em planos de controle com raiz. Um aplicativo agindo como a raiz criará \_ soquetes raiz c e as contrapartes em execução em nós folha utilizarão \_ soquetes de folha c. O aplicativo raiz usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para adicionar novos nós folha. Os aplicativos correspondentes nos nós folha terão definido seus \_ soquetes folha c no modo de escuta. **WSAJoinLeaf** com um \_ soquete raiz c especificado é mapeado para a mensagem de addparting do Q. 2931. A junção iniciada por folha não tem suporte no ATM UNI 3,1, mas tem suporte no ATM UNI 4,0. Portanto, **WSAJoinLeaf** com um \_ soquete folha c especificado é mapeado para a mensagem ATM UNI 4,0 apropriada.

Há considerações adicionais a serem lembradas para o ponto a multiponto do ATM:

-   A adição de novas folhas à sessão de ponto a multiponto ATM é apenas baseada em convite. As convites raiz saem, que já têm sua chamada de função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) – chamando a função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   O fluxo de dados em uma sessão de ponto a multiponto ATM é somente de raiz para sair; as folhas não podem usar a mesma sessão para enviar informações para a raiz.
-   Apenas uma folha por adaptador ATM é permitida.

 

 



