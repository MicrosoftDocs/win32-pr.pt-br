---
description: O atributo Color especifica a cor da caneta.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Cor da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502405"
---
# <a name="pen-color"></a>Cor da caneta

O atributo Color especifica a cor da caneta. Um aplicativo pode criar uma caneta superficial com uma cor exclusiva usando a macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) para armazenar o terceto vermelho, verde e azul que especifica a cor desejada em uma estrutura [COLORREF](colorref.md) e passando o endereço dessa estrutura para a função [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . (As canetas de estoque são limitadas a preto, branco e invisível.) Para obter mais informações sobre tercetos e cores RGB, consulte [cores](colors.md).

 

 



