---
description: A coleção Strokes analisada pelo objeto divisória é mantida na Propriedade Strokes do objeto divisória.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Trabalhando com uma coleção de traços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35673ef17882f246969e7c74869f47b09b604195c74bb1456c3624713a42045d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221866"
---
# <a name="working-with-a-strokes-collection"></a>Trabalhando com uma coleção de traços

A coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analisada pelo objeto [**divisória**](inkdivider-class.md) é mantida na propriedade [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) do objeto **divisória** . Como uma coleção **Strokes** é uma referência a dados de tinta e não é os dados reais propriamente dito, as alterações no objeto [**Ink**](inkdisp-class.md) pai da coleção **Strokes** podem invalidar a coleção **Strokes** . Para obter mais informações sobre dados de tinta, consulte [dados de tinta](ink-data.md). Para obter mais informações sobre a coleta de tinta, consulte [coleta de tinta](ink-collection.md).

Para manter a [**Propriedade Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) do objeto [**divisória**](inkdivider-class.md) sincronizado com um objeto [**Ink**](inkdisp-class.md) , use os eventos [**InkAdded**](inkdisp-inkadded.md) e [**InkDeleted**](inkdisp-inkdeleted.md) do objeto **Ink** para ouvir os traços que devem ser adicionados ou removidos do objeto **divisória** . Isso abrange casos em que os traços são adicionados a, excluídos de, recortados ou divididos dentro do objeto de **tinta** . Mover, dimensionar ou outras transformações em traços no objeto de **tinta** não gera eventos **InkAdded** ou **InkDeleted** . Para refletir essa transformação na propriedade **Strokes** do objeto **divisória** , execute a mesma transformação nos traços no objeto **divisória** .

A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) contém uma cópia dos traços no objeto [**divisória**](inkdivider-class.md) no momento em que o objeto **DivisionResult** foi criado. Você pode comparar as propriedades de **traços** de dois objetos **DivisionResult** para determinar se os traços foram alterados entre as duas vezes que o método de [**divisão**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) foi chamado.

A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) do objeto [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) contém o subconjunto dos traços no objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que correspondem a esse elemento. Você pode passar esses traços para um [**RecognizerContext**](inkrecognizercontext-class.md) separado para obter um resultado de reconhecimento para o elemento. Como os elementos manuscritos existem em diferentes níveis de detalhes, as coleções de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para diferentes elementos podem se sobrepor. Por exemplo, a coleção **Strokes** para um elemento de segmento de reconhecimento será um subconjunto da coleção **Strokes** para o elemento line do qual o segmento de reconhecimento faz parte.

 

 
