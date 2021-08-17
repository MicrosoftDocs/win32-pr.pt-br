---
description: O objeto DivisionUnit representa um único elemento estrutural de um objeto DivisionResult. Um objeto DivisionUnit pode representar um desenho, um único segmento de reconhecimento de manuscrito, uma linha de manuscrito ou um bloco de manuscrito.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Trabalhando com o objeto DivisionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c2ce09bf2b67f5724bba523219d0555063c3f7215810d3b11c48596f979fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966505"
---
# <a name="working-with-the-divisionunit-object"></a>Trabalhando com o objeto DivisionUnit

O objeto **DivisionUnit** representa um único elemento estrutural de um objeto **DivisionResult** . Um objeto **DivisionUnit** pode representar um desenho, um único segmento de reconhecimento de manuscrito, uma linha de manuscrito ou um bloco de manuscrito.

A enumeração [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define os tipos de elementos estruturais que a análise de layout reconhece. Na automação, o objeto **DivisionUnit** é chamado de [**IInkDivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit).

A propriedade [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) do objeto **DivisionUnit** retorna o tipo de elemento estrutural que o objeto **DivisionUnit** é. A propriedade [**RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) do objeto **DivisionUnit** retorna o texto de reconhecimento para elementos manuscritos ou **NULL** para elementos de desenho.

A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) do objeto **DivisionUnit** contém o subconjunto dos traços no objeto **DivisionResult** que correspondem a esse elemento. Como os elementos manuscritos existem para diferentes níveis de detalhes, as coleções de **traços** para diferentes elementos podem se sobrepor. Especificamente, um segmento de reconhecimento compartilha traços com a linha e o bloco é parte do, e uma linha compartilha traços com o bloco do qual faz parte.

A propriedade [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) do objeto **DivisionUnit** retorna uma matriz para girar os traços do elemento para horizontal. Para elementos de parágrafo e desenho, a propriedade **RotationTransform** retorna a matriz de identidade. Um reconhecedor de texto tem um desempenho muito melhor no manuscrito que é horizontalmente alinhado do que no manuscrito que não é. Na automação, isso é chamado de propriedade **RotationTransform** e retorna um objeto [**InkTransform**](inktransform-class.md) que contém a matriz de transformação. A propriedade **RotationTransform** retorna **NULL** para elementos de parágrafo e de desenho.

Para obter mais informações sobre o objeto **DivisionResult** , consulte [trabalhando com o objeto DivisionResult](working-with-the-divisionresult-object.md).

 

 
