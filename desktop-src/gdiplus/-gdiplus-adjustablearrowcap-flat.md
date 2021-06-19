---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções simples de API são encapsuladas pela classe AdjustableArrowCap C++.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: Funções AdjustableArrowCap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9ee90ea50c4b487ceb90e1b30f1329151533
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395071"
---
# <a name="adjustablearrowcap-functions"></a>Funções AdjustableArrowCap

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

As funções de API simples a seguir são encapsuladas pela classe [**AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) C++.

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Funções AdjustableArrowCap e métodos wrapper correspondentes



| Função Flat                                                                                                          | Método de wrapper                                                                                                                | Descrição                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap (altura REAL, largura REAL, BOOL ispreenchad, GpAdjustableArrowCap \* \* Cap) | [**AdjustableArrowCap::AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Cria uma extremidade de linha de seta ajustável com a altura e a largura especificadas. A extremidade da linha de seta pode ser preenchida ou não-preenchida. A margem interna do meio padrão é zero.                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight (GpAdjustableArrowCap \* Cap, real Height)                           | [**AdjustableArrowCap:: SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | O método [**AdjustableArrowCap:: SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) define a altura da Cap da seta. Essa é a distância da base da seta para seu vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight (GpAdjustableArrowCap \* Cap, real \* Height)                         | [**AdjustableArrowCap:: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | O método [**AdjustableArrowCap:: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) Obtém a altura da Cap da seta. A altura é a distância da base da seta até seu vértice.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth (GpAdjustableArrowCap \* Cap, largura real)                             | [**AdjustableArrowCap:: SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | O método [**AdjustableArrowCap:: SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) define a largura da Cap da seta. A largura é a distância entre os pontos de extremidade da base da seta.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth (GpAdjustableArrowCap \* Cap, \* largura real)                           | [**AdjustableArrowCap:: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | O método [**AdjustableArrowCap:: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) Obtém a largura da Cap da seta. A largura é a distância entre os pontos de extremidade da base da seta.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* Cap, real middleInset)                 | [**AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | O método [**AdjustableArrowCap:: SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) define o número de unidades que o ponto médio da base muda até o vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* Cap, real \* middleInset)<br/>    | [**AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | O método [**AdjustableArrowCap:: GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) Obtém o valor da inserção. A margem intermediária é o número de unidades que o ponto médio da base muda para o vértice. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState (GpAdjustableArrowCap \* Cap, bool fillstate)<br/>          | [**AdjustableArrowCap:: setfillstate**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | O método [**AdjustableArrowCap:: Setfillstate**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) define o estado de preenchimento da Cap da seta. Se a tampa da seta não for preenchida, apenas a estrutura de tópicos será desenhada.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState (GpAdjustableArrowCap \* Cap, bool \* fillstate)<br/>        | [**AdjustableArrowCap:: ispreenchad**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | O método [**AdjustableArrowCap:: IsCompleted**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) determina se a tampa da seta está preenchida.                                                                                               |



 

 

