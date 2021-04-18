---
description: Contém uma coleção de objetos que implementam a interface IAnalysisAlternate e que são o resultado da análise de tinta.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interface IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788859"
---
# <a name="ianalysisalternates-interface"></a>Interface IAnalysisAlternates

Contém uma coleção de objetos que implementam a interface [**IAnalysisAlternate**](ianalysisalternate.md) e que são o resultado da análise de tinta.

## <a name="members"></a>Membros

A interface **IAnalysisAlternates** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternates** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAnalysisAlternates** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | Recupera o objeto [**IAnalysisAlternate**](ianalysisalternate.md) no índice especificado dentro da coleção.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Recupera o número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contidos na coleção **IAnalysisAlternates** .<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface é equivalente à classe [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) na .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**Método IInkAnalyzer:: getalternations**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

