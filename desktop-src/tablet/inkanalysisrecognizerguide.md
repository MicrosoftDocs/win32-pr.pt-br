---
description: Especifica o guia ou a área em que a tinta é desenhada e reconhecida.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Estrutura InkAnalysisRecognizerGuide (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790462"
---
# <a name="inkanalysisrecognizerguide-structure"></a>Estrutura InkAnalysisRecognizerGuide

Especifica o guia ou a área em que a tinta é desenhada e reconhecida.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a>Membros

<dl> <dt>

**rectWritingBox**
</dt> <dd>

A área de escrita invisível do guia de reconhecimento no qual a gravação pode realmente ocorrer.

</dd> <dt>

**rectDrawnBox**
</dt> <dd>

O retângulo que é desenhado na tela do Tablet e em que ocorre a gravação.

</dd> <dt>

**Rapina**
</dt> <dd>

O número de linhas na caixa guia de reconhecimento.

</dd> <dt>

**cColumns**
</dt> <dd>

O número de colunas na caixa guia de reconhecimento.

</dd> <dt>

**Tabs no meio**
</dt> <dd>

A altura de Tabs no meio da caixa do guia de reconhecimento. A altura de Tabs no meio é a distância da linha de base para o Tabs no meio da caixa de desenho.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um **InkAnalysisRecognizerGuide** define uma área esperada de entrada, como uma linha ou caixas, para caracteres. Uma estrutura **InkAnalysisRecognizerGuide** pode ser definida somente em um nó de contexto de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)). O [**IInkAnalyzer**](iinkanalyzer.md) usa o local do nó de dica de análise e os locais dos traços de tinta para associar um traço ao nó de dica de análise. Todos os traços com uma associação ao nó de dica de análise terão o **InkAnalysisRecognizerGuide** especificado usado quando reconhecidos por um **IInkAnalyzer**, desde que o **IInkAnalyzer** dê suporte ao **InkAnalysisRecognizerGuide**. Os valores expressos na classe **InkAnalysisRecognizerGuide** são sempre relativos ao local do nó de dica de análise e são especificados em coordenadas de espaço de tinta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da dica de análise](analysis-hint-properties.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




