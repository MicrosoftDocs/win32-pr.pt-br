---
description: Esta seção contém um exemplo que demonstra a criação de uma imagem e o processo de armazenar os registros correspondentes em um metarquivo.
ms.assetid: 8be95fef-93dc-4c9c-a0d3-840918c00e43
title: Exibindo uma imagem e armazenando-a em um metarquivo avançado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8eee65f2f82a7b8ccdad86e99987df6a06a4f5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661615"
---
# <a name="displaying-a-picture-and-storing-it-in-an-enhanced-metafile"></a>Exibindo uma imagem e armazenando-a em um metarquivo avançado

Esta seção contém um exemplo que demonstra a criação de uma imagem e o processo de armazenar os registros correspondentes em um metarquivo. O exemplo desenha uma imagem para a exibição ou a armazena em um metarquivo. Se um identificador de contexto de dispositivo de vídeo for fornecido, ele desenhará uma imagem na tela usando várias funções GDI. Se um contexto de dispositivo de metarquivo avançado for fornecido, ele armazenará a mesma imagem no metarquivo avançado.


```C++
void DrawOrStore(HWND hwnd, HDC hdcMeta, HDC hdcDisplay) 
{ 
 
RECT rect; 
HDC hDC; 
int fnMapModeOld; 
HBRUSH hbrOld; 
 
// Draw it to the display DC or store it in the metafile device context.  
 
if (hdcMeta) 
    hDC = hdcMeta; 
else 
    hDC = hdcDisplay; 
 
// Set the mapping mode in the device context.  
 
fnMapModeOld = SetMapMode(hDC, MM_LOENGLISH); 
 
// Find the midpoint of the client area.  
 
GetClientRect(hwnd, (LPRECT)&rect); 
DPtoLP(hDC, (LPPOINT)&rect, 2); 
 
// Select a gray brush.  
 
hbrOld = SelectObject(hDC, GetStockObject(GRAY_BRUSH)); 
 
// Draw a circle with a one inch radius.  
 
Ellipse(hDC, (rect.right/2 - 100), (rect.bottom/2 + 100), 
       (rect.right/2 + 100), (rect.bottom/2 - 100)); 
 
// Perform additional drawing here.  
 
 
 
// Set the device context back to its original state.  
 
SetMapMode(hDC, fnMapModeOld); 
SelectObject(hDC, hbrOld); 
} 
```



 

 



