---
description: Indica se um traço deve ser analisado como parte de um desenho ou como parte da escrita.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumeração StrokeType (IACom.h)
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
ms.openlocfilehash: 4b02a05582d675f04ad4458b1cb21c6d4a1797bacf15baf5d0851804d1a95d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589576"
---
# <a name="stroketype-enumeration"></a>Enumeração StrokeType

Indica se um traço deve ser analisado como parte de um desenho ou como parte da escrita.

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

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType \_ Não Classificado**
</dt> <dd>

O traço pode fazer parte de um desenho ou parte da escrita.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Escrita de \_ StrokeType**
</dt> <dd>

O traço faz parte da escrita.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**Desenho de \_ StrokeType**
</dt> <dd>

O traço faz parte de um desenho.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra parte de um manipulador de eventos de traço, implementado de maneira semelhante ao Exemplo de Sinks de Eventos [C++.](c---event-sinks-sample.md) O traço adicionado é verificado para ver se a parte superior da caixa delimitada foi desenhada abaixo de uma margem, `drawingMargin` . Se sim, o [**objeto IInkAnalyzer,**](iinkanalyzer.md) , é definido para analisar o traço como um traço de desenho, em vez de como `m_spInkAnalyzer` um traço de manuscrito. `CheckHResult`é uma função que aceita uma cadeia de caracteres e e lança uma exceção criada com a cadeia de `HRESULT` caracteres se `HRESULT` o não for **SUCCESS.**


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
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IInkAnalyzer::SetRogkeType**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




