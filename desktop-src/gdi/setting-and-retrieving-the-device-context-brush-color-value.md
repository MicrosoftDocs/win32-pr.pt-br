---
description: O exemplo a seguir mostra como um aplicativo pode recuperar a cor do pincel do DC atual usando as funções SetDCBrushColor e GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Configurando e recuperando o valor de cor do pincel de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d2f99f80305336af74a775b6f090c678ab60dcc6fed6fe29e62d03aea98001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698195"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a>Configurando e recuperando o valor de cor do pincel de contexto do dispositivo

O exemplo a seguir mostra como um aplicativo pode recuperar a cor do pincel do DC atual usando as funções [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) e [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) .


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc,RGB(00,0xff,00));
PatBlt(hdc,0,0,200,200,PATCOPY);
SetDCBrushColor(hdc,RGB(00,00,0xff));
PatBlt(hdc,0,0,200,200,PATCOPY);
```



 

 



