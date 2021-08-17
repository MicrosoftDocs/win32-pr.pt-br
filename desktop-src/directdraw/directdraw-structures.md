---
title: Estruturas do DirectDraw
description: Esta seção contém informações sobre as seguintes estruturas usadas com o DirectDraw
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba62751b619982628575b380ea75eb57661db8737325fee1fb1b042e856ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504338"
---
# <a name="directdraw-structures"></a>Estruturas do DirectDraw

Esta seção contém informações sobre as seguintes estruturas usadas com o DirectDraw:

-   [**DDBLTBATCH**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [**Ddbltfx**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [**Ddcaps**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [**Ddcolorcontrol**](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [**Ddcolorkey**](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [**DDDEVICEIDENTIFIER2**](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [**DDGAMMARAMP**](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [**DDOVERLAYFX**](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [**Ddpixelformat**](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   [**Ddscaps**](/previous-versions/ms783271(v=vs.85))
-   [**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))
-   [**Ddsurfacedesc**](/previous-versions/ms783272(v=vs.85))
-   [**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))

> [!Note]  
> Você deve inicializar a memória de cada estrutura DirectX como 0 antes de usar a estrutura . Além disso, para todas as estruturas que contêm um membro **dwSize,** você deve definir o membro para o tamanho da estrutura, em bytes, antes que a estrutura seja usada. O exemplo a seguir executa essas tarefas em uma estrutura comum, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




