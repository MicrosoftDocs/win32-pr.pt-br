---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funções de pincel (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296670"
---
# <a name="brush-functions-gdi"></a>Funções de pincel (GDI+)

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

As seguintes funções simples de API são encapsuladas pela classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funções de pincel e métodos wrapper correspondentes



| Função Flat                                                                        | Método de wrapper                                          | Description                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)          | [**Pincel:: clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | O método [**Brush:: clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) cria um novo objeto de [**pincel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) com base neste pincel. |
| GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)                                 | virtual ~ Brush ()                                        | Limpa os recursos usados por um objeto de [**pincel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* pincel, \* tipo GpBrushType)<br/> | [**Pincel:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | O método [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) Obtém o tipo desse pincel.                                                      |



 

 

 




