---
description: Recupera 10 alternativas de análise para toda a tinta associada ao IInkAnalyzer.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'Método IInkAnalyzer:: getalternations (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779980"
---
# <a name="iinkanalyzergetalternates-method"></a>Método IInkAnalyzer:: getalternations

Recupera 10 alternativas de análise para toda a tinta associada ao [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAlternates* \[ fora\]
</dt> <dd>

Um ponteiro para os 10 principais objetos [**IAnalysisAlternate**](ianalysisalternate.md) para toda a tinta associada ao [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAlternates* quando você não precisar mais usar o objeto.

 

A alternativa superior é retornada como a primeira alternativa da coleção.

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

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

