---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe C++ SolidBrush.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funções SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395551"
---
# <a name="solidbrush-functions"></a>Funções SolidBrush

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas no Gdiplus.dll e declaradas em Gdiplusflat.h. As funções na API simples GDI+ são envolvidas por uma coleção de cerca de 40 classes C++. É recomendável não chamar as funções na API simples diretamente. Sempre que você fizer chamadas para GDI+, recomendamos que você faça isso chamando os métodos e funções fornecidos pelos wrappers do C++. Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [API simples GDI+.](-gdiplus-flatapi-flat.md)

As funções de API simples a seguir são empacotadas pela [**classe C++ SolidBrush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funções de pincel e métodos de wrapper correspondentes



| Função simples                                                                               | Método Wrapper                                                                                       | Comentários                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill(cor ARGB, pincel \* \* GpSolidFill)**<br/>   | [**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Cria um [**objeto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) com base em uma cor |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor(pincel GpSolidFill, \* cor ARGB)**<br/>   | [**SolidBrush::SetColor(IN const Color& color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Define a cor desse pincel sólido                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor(pincel GpSolidFill, \* cor \* ARGB)**<br/> | [**SolidBrush::GetColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Obtém a cor desse pincel sólido                                                      |



 

 

 
