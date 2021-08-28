---
description: Indica o nível de confiança que o IInkAnalyzer tem na precisão do resultado do reconhecimento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumeração RecognitionConfidence (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b5943b303c01a681b1df9d6d919df1822a5f2345c85fb5c52e3ab865ee58dd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596626"
---
# <a name="recognitionconfidence-enumeration"></a>Enumeração RecognitionConfidence

Indica o nível de confiança que o [**IInkAnalyzer**](iinkanalyzer.md) tem na precisão do resultado do reconhecimento.

## <a name="syntax"></a>Syntax


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ Strong**
</dt> <dd>

Forte confiança no resultado ou alternativo.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermediário**
</dt> <dd>

Confiança intermediária no resultado ou alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ ruim**
</dt> <dd>

Má confiança no resultado ou alternativo.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ desconhecido**
</dt> <dd>

O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que gerou o texto reconhecido não dá suporte a níveis de confiança.

</dd> </dl>

## <a name="remarks"></a>Comentários

O [**IInkAnalyzer**](iinkanalyzer.md) usa um ou mais objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para converter manuscrito em texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IAnalysisAlternate:: GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Propriedades do nó de contexto](context-node-properties.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




