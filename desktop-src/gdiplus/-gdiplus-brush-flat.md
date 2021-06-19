---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funções brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395081"
---
# <a name="brush-functions-gdi"></a>Funções brush (GDI+)

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas no Gdiplus.dll e declaradas em Gdiplusflat.h. As funções na API simples GDI+ são envolvidas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que fizer chamadas ao GDI+, você deverá fazer isso chamando os métodos e funções fornecidos pelos wrappers do C++. Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [API simples GDI+.](-gdiplus-flatapi-flat.md)

As funções de API simples a seguir são empacotadas pela [**classe Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funções de pincel e métodos de wrapper correspondentes



| Função simples                                                                        | Método Wrapper                                          | Descrição                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush(pincel GpBrush, \* \* \* cloneBrushBrush)          | [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | O [**método Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) cria um novo [**objeto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) com base nesse pincel. |
| GpStatus WINGDIPAPI GdipDeleteBrush(pincel \* GpBrush)                                 | virtual ~Brush()                                        | Limpa os recursos usados por um [**objeto Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType(pincel GpBrush, \* tipo GpBrushType) \*<br/> | [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | O [**método Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtém o tipo desse pincel.                                                      |



 

 

 




