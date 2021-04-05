---
description: Recupera uma coleção ordenada de objetos IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827173"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority

Recupera uma coleção ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppInkAnalysisRecognizers* \[ fora\]
</dt> <dd>

Uma coleção ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppInkAnalysisRecognizers* quando você não precisar mais usar o objeto.

 

A ordem dos reconhecedores nesta coleção indica a ordem na qual o [**IInkAnalyzer**](iinkanalyzer.md) avalia os reconhecedores disponíveis. O **IInkAnalyzer** usa a linguagem dos traços como seu critério principal para aplicar um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Como um critério secundário, o **IInkAnalyzer** compara as informações de dica de análise com os recursos com suporte de um objeto **IInkAnalysisRecognizer** (consulte [**IInkAnalysisRecognizer:: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)). Para obter mais informações sobre dicas de análise, consulte [**método IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md).

Se mais de um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) der suporte a um identificador de idioma, o [**IInkAnalyzer**](iinkanalyzer.md) usará um algoritmo "primeiro ajuste" para selecionar o primeiro **IInkAnalysisRecognizer** para analisar os traços desse idioma.

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

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

