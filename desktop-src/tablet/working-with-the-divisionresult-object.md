---
description: O objeto DivisionResult representa um instantâneo da análise de layout dos traços contidos no objeto divisória. Ele contém a classificação de traço e as informações de agrupamento da análise de layout.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Trabalhando com o objeto DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b1bb001ecc57c0925253b01b129e0c6fcf0c0243c5a77f0eb697e2cc5c618d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715066"
---
# <a name="working-with-the-divisionresult-object"></a>Trabalhando com o objeto DivisionResult

O objeto **DivisionResult** representa um instantâneo da análise de layout dos traços contidos no objeto **divisória** . Ele contém a classificação de traço e as informações de agrupamento da análise de layout.

Você pode obter informações do objeto **DivisionResult** por tipo de elemento estrutural, como desenho ou linhas de manuscrito. O objeto **DivisionResult** pode persistir depois que o objeto **divisória** é destruído. Na automação, esse objeto é chamado de objeto de [**interface IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do objeto **DivisionResult** contém uma cópia da coleção **Strokes** no objeto **divisória** no momento em que o objeto **DivisionResult** foi criado.

A enumeração [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define os tipos de elementos estruturais que a análise de layout reconhece.

O método [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) do objeto **DivisionResult** retorna uma coleção **DivisionUnits** que contém todos os elementos estruturais de um determinado tipo. Um elemento estrutural individual é representado por um objeto **DivisionUnit** . Sempre que você chamar o método **ResultByType** , o objeto **DivisionResult** criará uma coleção **DivisionUnits** . Para obter mais informações sobre o objeto **DivisionUnit** , consulte [trabalhando com o objeto DivisionUnit](working-with-the-divisionunit-object.md).

 

 
