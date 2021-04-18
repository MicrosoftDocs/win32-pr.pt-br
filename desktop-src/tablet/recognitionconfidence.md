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
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785113"
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
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



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

 

 




