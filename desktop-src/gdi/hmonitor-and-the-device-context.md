---
description: Cada exibição física é representada por um identificador de monitor do tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR e o contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb727457c388710b19d8f22bef8f65d76e9d8c5c27b0ec7dfcbf55a4acea3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558746"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR e o contexto do dispositivo

Cada exibição física é representada por um identificador de monitor do tipo **HMONITOR.** Um **HMONITOR válido** é garantido como não NULL. Uma exibição física tem o **mesmo HMONITOR,** desde que ele seja parte da área de trabalho. Quando uma **mensagem WM \_ DISPLAYCHANGE** é enviada, qualquer monitor pode ser removido da área de trabalho e, portanto, seu **HMONITOR** se torna inválido ou tem suas configurações alteradas. Portanto, um aplicativo deve verificar se todos **os HMONITORS são** válidos quando essa mensagem é enviada.

Qualquer função que retorna um DC (contexto de dispositivo de exibição) normalmente retorna um DC para o monitor primário. Para obter o DC para outro monitor, use a [**função EnumDisplayMonitors.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) Ou você pode usar o nome do dispositivo da [**função GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para criar um DC com [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca). No entanto, se a função, como [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)obter um DC para uma janela que abrange mais de uma exibição, o controlador de dc também abrange as duas exibições.

 

 



