---
description: Quando aplicativos de desenho complexos executam operações gráficas demoradas, eles consomem recursos valiosos do sistema.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Cancelamento de operações de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2ddf90842ed7da612e046f8cc44bc8972b236232f3757bd31a295377eafab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470026"
---
# <a name="cancellation-of-drawing-operations"></a>Cancelamento de operações de desenho

Quando aplicativos de desenho complexos executam operações gráficas demoradas, eles consomem recursos valiosos do sistema. Aproveitando os recursos multitarefa do sistema, um aplicativo pode usar threads e a [**função CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) para gerenciar essas operações. Por exemplo, se a operação de gráficos executada pelo thread A estiver consumindo recursos necessários, o thread B poderá chamar a função CancelDC para interromper essa operação.

 

 



