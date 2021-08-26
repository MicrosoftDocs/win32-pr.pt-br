---
description: Cada monitor pode ter sua própria profundidade de cor.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Cores em vários monitores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd799599f3818ad002ee8a0fa1e9478f383b3052dd3a2cc3b8a40843e431b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115316"
---
# <a name="colors-on-multiple-display-monitors"></a>Cores em vários monitores de vídeo

Cada monitor pode ter sua própria profundidade de cor. O sistema ajusta automaticamente as cores à medida que o Windows se move entre monitores com profundidades de cores diferentes. Em geral, isso produz bons resultados. No entanto, isso nem sempre é o ideal. Para aproveitar os recursos de cores de monitores diferentes, consulte a seção [pintando vários monitores de vídeo](painting-on-multiple-display-monitors.md) , a seguir.

Para determinar se todos os monitores têm o mesmo formato de cor, chame [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com SM \_ SAMEDISPLAYFORMAT.

Se o monitor primário for palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funcionam da mesma forma que antes, mas em todos os monitores. Além disso, as paletas de todos os dispositivos palettized são sincronizadas. Se o monitor primário não for palettized, **SelectPalette** e **RealizePalette** selecionarão a paleta em segundo plano e os dispositivos de palettized não serão sincronizados.

 

 
