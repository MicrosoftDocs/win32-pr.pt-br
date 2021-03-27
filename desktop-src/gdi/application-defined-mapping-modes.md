---
description: Os dois modos de mapeamento definidos pelo aplicativo (MM \_ ISOTROPIC e mm \_ ANISOTROPIC) são fornecidos para modos de mapeamento específicos do aplicativo.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Modos de mapeamento de Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988847"
---
# <a name="application-defined-mapping-modes"></a>Modos de mapeamento de Application-Defined

Os dois modos de mapeamento definidos pelo aplicativo (MM \_ ISOTROPIC e mm \_ ANISOTROPIC) são fornecidos para modos de mapeamento específicos do aplicativo. O \_ modo ISOTROPIC de mm garante que as unidades lógicas na direção x e na direção y sejam iguais, enquanto o \_ modo ANISOTROPIC mm permite que as unidades sejam diferentes. Um aplicativo CAD ou de desenho pode se beneficiar do \_ modo de mapeamento ISOTROPIC mm, mas pode ser necessário especificar unidades lógicas que correspondam aos incrementos na escala de um engenheiro (1/64 polegadas). Essas unidades seriam difíceis de obter com os modos de mapeamento predefinidos (MM \_ HIENGLISH ou mm \_ HIMETRIC); no entanto, elas podem ser obtidas facilmente selecionando o \_ modo mm ISOTROPIC (ou mm \_ ANISOTROPIC). O exemplo a seguir mostra como definir unidades lógicas como 1/64 polegadas:


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



