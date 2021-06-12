---
description: O exemplo a seguir mostra como um aplicativo pode recuperar a cor do pincel do DC atual usando as funções SetDCBrushColor e GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Configurando e recuperando o valor de cor do pincel de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0bfc918f5882baa46208d27973e14b9446909e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010629"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a><span data-ttu-id="2126b-103">Configurando e recuperando o valor de cor do pincel de contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="2126b-103">Setting and Retrieving the Device Context Brush Color Value</span></span>

<span data-ttu-id="2126b-104">O exemplo a seguir mostra como um aplicativo pode recuperar a cor do pincel do DC atual usando as funções [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) e [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) .</span><span class="sxs-lookup"><span data-stu-id="2126b-104">The following example shows how an application can retrieve the current DC brush color by using the [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) and the [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) functions.</span></span>


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc,RGB(00,0xff,00));
PatBlt(hdc,0,0,200,200,PATCOPY);
SetDCBrushColor(hdc,RGB(00,00,0xff));
PatBlt(hdc,0,0,200,200,PATCOPY);
```



 

 



