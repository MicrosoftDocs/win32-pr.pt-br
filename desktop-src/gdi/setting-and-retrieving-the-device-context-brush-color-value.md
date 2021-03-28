---
description: O exemplo a seguir mostra como um aplicativo pode recuperar a cor do pincel do DC atual usando as funções SetDCBrushColor e GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Configurando e recuperando o valor de cor do pincel de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c684bfd50fd92959e9b8f7eac5baf96c62fd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988960"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a>Configurando e recuperando o valor de cor do pincel de contexto do dispositivo

O exemplo a seguir mostra como um aplicativo pode recuperar a cor do pincel do DC atual usando as funções [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) e [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) .


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc, RGB(00,0xff;00);
PatBlt(0,0,200,200,PATCOPY)
SetDCBrushColor(hdc,RGB(00,00,0xff);
PatBlt(0,0,200,200,PATCOPY);
```



 

 



