---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funções SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967399"
---
# <a name="solidbrush-functions"></a>Funções SolidBrush

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++. Recomendamos não chamar as funções na API simples diretamente. Sempre que você fizer chamadas para GDI+, recomendamos que faça isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

As funções de API simples a seguir são encapsuladas pela classe [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funções de pincel e métodos wrapper correspondentes



| Função Flat                                                                               | Método de wrapper                                                                                       | Comentários                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill (cor ARGB, pincel de GpSolidFill \* \* )**<br/>   | [**SolidBrush:: SolidBrush (IN const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Cria um objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) com base em uma cor |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, cor ARGB)**<br/>   | [**SolidBrush:: setColor (na cor const& cor)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Define a cor deste pincel sólido                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, \* cor ARGB)**<br/> | [**Const SolidBrush:: GetColor (fora da cor da cor \* )**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Obtém a cor deste pincel sólido                                                      |



 

 

 
