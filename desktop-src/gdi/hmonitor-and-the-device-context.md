---
description: Cada exibição física é representada por um identificador de monitor do tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR e o contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988808"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR e o contexto do dispositivo

Cada exibição física é representada por um identificador de monitor do tipo **HMONITOR**. Uma **HMONITOR** válida é garantida como não nula. Uma exibição física tem o mesmo **HMONITOR** , desde que faça parte da área de trabalho. Quando uma mensagem do **WM \_ DISPLAYCHANGE** é enviada, qualquer monitor pode ser removido da área de trabalho e, portanto, seu **HMONITOR** se torna inválido ou tem suas configurações alteradas. Portanto, um aplicativo deve verificar se todos os **HMONITORS** são válidos quando essa mensagem é enviada.

Qualquer função que retorne um DC (contexto de dispositivo de exibição) normalmente retorna um DC para o monitor primário. Para obter o controlador de domínio para outro monitor, use a função [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) . Ou, você pode usar o nome do dispositivo da função [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para criar um controlador de domínio com [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca). No entanto, se a função, como [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), obtém um DC para uma janela que abrange mais de uma exibição, o DC também abrangerá as duas exibições.

 

 



