---
description: Indica se um traço deve ser analisado como parte de um desenho ou como parte da gravação.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumeração StrokeType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170688"
---
# <a name="stroketype-enumeration"></a>Enumeração StrokeType

Indica se um traço deve ser analisado como parte de um desenho ou como parte da gravação.

## <a name="syntax"></a>Syntax


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType não \_ classificado**
</dt> <dd>

O traço pode ser qualquer parte de um desenho ou parte da escrita.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Escrita de StrokeType \_**
</dt> <dd>

O traço faz parte da gravação.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**Desenho de StrokeType \_**
</dt> <dd>

O traço faz parte de um desenho.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra parte de um manipulador de eventos de traço, implementado de maneira semelhante ao [exemplo de coletores de eventos C++](c---event-sinks-sample.md). O traço adicionado é verificado para ver se a parte superior da caixa delimitadora foi desenhada abaixo de uma margem, `drawingMargin` . Nesse caso, o objeto [**IInkAnalyzer**](iinkanalyzer.md) , `m_spInkAnalyzer` , é definido para analisar o traço como um traço de desenho, e não como um traço de manuscrito. `CheckHResult` é uma função que usa um `HRESULT` e uma cadeia de caracteres e gera uma exceção criada com a cadeia de caracteres se o `HRESULT` não for **êxito**.


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IInkAnalyzer:: setstroketype**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




