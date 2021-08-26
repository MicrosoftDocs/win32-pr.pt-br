---
description: Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções simples de API são encapsuladas pela classe SolidBrush C++.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funções SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0a45d36a174e765990f284d99d18a18d420745967b36cdd40d4a0ee7d1c0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014696"
---
# <a name="solidbrush-functions"></a>Funções SolidBrush

Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. as funções no GDI+ API simples são encapsuladas por uma coleção de cerca de 40 classes C++. Recomendamos não chamar as funções na API simples diretamente. sempre que você fizer chamadas para GDI+, recomendamos que faça isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente. para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ API simples](-gdiplus-flatapi-flat.md).

As funções de API simples a seguir são encapsuladas pela classe [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funções de pincel e métodos wrapper correspondentes



| Função Flat                                                                               | Método de wrapper                                                                                       | Comentários                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill (cor ARGB, pincel de GpSolidFill \* \* )**<br/>   | [**SolidBrush:: SolidBrush (IN const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Cria um objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) com base em uma cor |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, cor ARGB)**<br/>   | [**SolidBrush:: setColor (na cor const& cor)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Define a cor deste pincel sólido                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, \* cor ARGB)**<br/> | [**Const SolidBrush:: GetColor (fora da cor da cor \* )**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Obtém a cor deste pincel sólido                                                      |



 

 

 
