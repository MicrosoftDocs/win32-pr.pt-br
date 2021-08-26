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
ms.openlocfilehash: e2643ef8ea90d029aee6bd0673931d27e9987b0af0a898e854cb87d74a89c0af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058086"
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

Essa interface é equivalente ao [**System. Windows. Classe Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) na .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
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

 

