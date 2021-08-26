---
description: Move o IInkAnalysisRecognizer especificado para a primeira posição na lista de reconhecedores de tinta do objeto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: Método IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8404a2e1e89980ce5e8cadac1a468b3383d37d4952349f3702539975a304ac92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935206"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>Método IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer

Move o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado para a primeira posição na lista de reconhecedores de tinta do objeto [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalysisRecognizer* \[ Em\]
</dt> <dd>

O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) a ser colocado na primeira posição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Para obter a lista de reconhecedores de tinta em ordem de prioridade, chame o método [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Esse método não afeta a ordem do restante dos objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) na lista de reconhecedores de tinta do objeto [**IInkAnalyzer.**](iinkanalyzer.md)

A ordem dos reconhecedores de tinta retornados pelo Método [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica a ordem na qual [**o IInkAnalyzer**](iinkanalyzer.md) avalia os objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponíveis.

O uso dos reconhecedores de tinta é avaliado com base em seu pedido na lista.

Durante a análise de tinta, [**o IInkAnalyzer**](iinkanalyzer.md) itera pelos reconhecedores de tinta em sua lista até encontrar um reconhecedor que dá suporte à linguagem e outras propriedades dos traços. Esse reconhecedor é usado para reconhecimento de tinta para esses traços.

Se [**o IInkAnalyzer**](iinkanalyzer.md) não encontrar um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que dá suporte a um conjunto de traços durante a análise, o **IInkAnalyzer** gerará um [**IAnalysisWarning**](ianalysiswarning.md) com um código de aviso **de AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (consulte [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




