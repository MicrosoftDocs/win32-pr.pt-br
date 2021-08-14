---
description: O atributo Color especifica a cor da caneta.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Cor da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e88d73fc80f6fe02a6d9e1de1d33568c94e05768f113c8bee0754c5d8afb418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886201"
---
# <a name="pen-color"></a>Cor da caneta

O atributo Color especifica a cor da caneta. Um aplicativo pode criar uma caneta superficial com uma cor exclusiva usando a macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) para armazenar o terceto vermelho, verde e azul que especifica a cor desejada em uma estrutura [COLORREF](colorref.md) e passando o endereço dessa estrutura para a função [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . (As canetas de estoque são limitadas a preto, branco e invisível.) Para obter mais informações sobre tercetos e cores RGB, consulte [cores](colors.md).

 

 



