---
description: Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe AdjustableArrowCap C++.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: Funções AdjustableArrowCap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52487252c5b684cc762248b35c0fe5f45e8e3759993ba3b99ab01343b84c412d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977826"
---
# <a name="adjustablearrowcap-functions"></a>Funções AdjustableArrowCap

Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas no Gdiplus.dll e declaradas em Gdiplusflat.h. As funções na API GDI+ simples são empacotadas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que fizer chamadas para GDI+, você deverá fazer isso chamando os métodos e funções fornecidos pelos wrappers do C++. Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos wrapper, [consulte GDI+ API Simples.](-gdiplus-flatapi-flat.md)

As funções de API simples a seguir são empacotadas pela [**classe AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) C++.

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Funções AdjustableArrowCap e métodos wrapper correspondentes



| Função simples                                                                                                          | Método Wrapper                                                                                                                | Descrição                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap(real height, REAL width, BOOL isFilled, GpAdjustableArrowCap \* \* cap) | [**AdjustableArrowCap::AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Cria um limite de linha de seta ajustável com a altura e a largura especificadas. O limite de linha de seta pode ser preenchido ou não preenchido. O inset do meio assume como padrão zero.                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, altura REAL)                           | [**AdjustableArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | O [**método AdjustableArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) define a altura da ponta da seta. Essa é a distância da base da seta para seu vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, altura \* REAL)                         | [**AdjustableArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | O [**método AdjustableArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) obtém a altura da ponta da seta. A altura é a distância da base da seta para seu vértice.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, largura REAL)                             | [**AdjustableArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | O [**método AdjustableArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) define a largura do limite de seta. A largura é a distância entre os pontos de extremidade da base da seta.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, largura \* REAL)                           | [**AdjustableArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | O [**método AdjustableArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) obtém a largura da ponta da seta. A largura é a distância entre os pontos de extremidade da base da seta.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL middleInset)                 | [**AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | O [**método AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) define o número de unidades que o ponto médio da base desloca para o vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL \* middleInset)<br/>    | [**AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | O [**método AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) obtém o valor do inset. O inset intermediário é o número de unidades que o ponto médio da base desloca para o vértice. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL fillState)<br/>          | [**AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | O [**método AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) define o estado de preenchimento do limite de seta. Se a ponta da seta não estiver preenchida, somente o contorno será desenhado.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL \* fillState)<br/>        | [**AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | O [**método AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) determina se a ponta da seta está preenchida.                                                                                               |



 

 

