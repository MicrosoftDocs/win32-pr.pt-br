---
description: Altera a alternativa superior atual para o IAnalysisAlternate especificado.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296387"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a>Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation

Altera a alternativa superior atual para o [**IAnalysisAlternate**](ianalysisalternate.md)especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*alternativo* \[ no\]
</dt> <dd>

A análise alterna para definir como a nova alternativa principal.

</dd> <dt>

*fconfirmAutomatically* \[ no\]
</dt> <dd>

**Variante \_ TRUE** para definir todos os nós de contexto de folha de tinta que correspondem à análise alternada para um tipo de confirmação de **confirmation \_ NodeTypeAndProperties** (consulte [**IContextNode::**](icontextnode-isconfirmed.md) IsDeleted [**e confirmtype**](confirmationtype.md)); **Variante \_ FALSE** para definir todos os nós de contexto de folha de tinta que correspondem à análise alternada para um tipo de confirmação de **confirmações \_ nenhum**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Para obter alternativas de análise, use o método [**IInkAnalyzer:: Getalternations**](iinkanalyzer-getalternates.md), [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Para obter os objetos de nó de contexto associados a uma alternativa de análise, use o [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Para alterar o tipo de confirmação para um nó de contexto, use [**IContextNode:: Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Confirmação de análise de tinta**](confirmationtype.md)
</dt> <dt>

[Referência](ink-analysis-reference.md)
</dt> </dl>

 

 




