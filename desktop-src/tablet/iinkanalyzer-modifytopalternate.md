---
description: Altera a alternativa superior atual para a alternativa especificada e limpa o tipo de confirmação para todos os objetos IContextNode associados à alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Método IInkAnalyzer:: ModifyTopAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793615"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>Método IInkAnalyzer:: ModifyTopAlternate

Altera a alternativa superior atual para a alternativa especificada e limpa o tipo de confirmação para todos os objetos [**IContextNode**](icontextnode.md) associados à alternativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlternate* \[ no\]
</dt> <dd>

O objeto [**IAnalysisAlternate**](ianalysisalternate.md) que contém a nova alternativa Top.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Para obter alternativas de análise, use o método [**IInkAnalyzer:: Getalternations**](iinkanalyzer-getalternates.md), [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Para obter os objetos [**IContextNode**](icontextnode.md) associados a uma alternativa de análise, use o [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

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

[**Confirmtype**](confirmationtype.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




