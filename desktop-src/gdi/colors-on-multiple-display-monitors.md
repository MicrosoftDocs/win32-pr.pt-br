---
description: Cada monitor pode ter sua própria profundidade de cor.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Cores em vários monitores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921293"
---
# <a name="colors-on-multiple-display-monitors"></a>Cores em vários monitores de vídeo

Cada monitor pode ter sua própria profundidade de cor. O sistema ajusta automaticamente as cores à medida que o Windows se move entre monitores com profundidades de cores diferentes. Em geral, isso produz bons resultados. No entanto, isso nem sempre é o ideal. Para aproveitar os recursos de cores de monitores diferentes, consulte a seção [pintando vários monitores de vídeo](painting-on-multiple-display-monitors.md) , a seguir.

Para determinar se todos os monitores têm o mesmo formato de cor, chame [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com SM \_ SAMEDISPLAYFORMAT.

Se o monitor primário for palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funcionam da mesma forma que antes, mas em todos os monitores. Além disso, as paletas de todos os dispositivos palettized são sincronizadas. Se o monitor primário não for palettized, **SelectPalette** e **RealizePalette** selecionarão a paleta em segundo plano e os dispositivos de palettized não serão sincronizados.

 

 
