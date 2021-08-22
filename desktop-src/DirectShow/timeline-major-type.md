---
description: A enumeração de tipo principal da linha do tempo \_ \_ especifica o tipo principal de um objeto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Enumeração de TIMELINE_MAJOR_TYPE (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: b18088a9d01b263c80a4ff941a6b7720043da708eaeaebf4f79a2084d1ed258f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501716"
---
# <a name="timeline_major_type-enumeration"></a>\_Enumeração de tipo principal de linha do tempo \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `TIMELINE_MAJOR_TYPE` enumeração Especifica o tipo principal de um objeto.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**LINHA de tempo \_ \_ tipo principal \_ composto**
</dt> <dd>

Objeto composto. Mantém uma ou mais faixas.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**LINHA \_ do \_ tipo principal \_ faixa**
</dt> <dd>

Rastrear objeto. Contém uma ou mais fontes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**LINHA de tempo \_ principal \_ tipo \_ fonte**
</dt> <dd>

Objeto de origem. Contém uma referência a uma fonte de mídia.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**LINHA do tempo de \_ \_ transição de tipo principal \_**
</dt> <dd>

Objeto de transição. Define uma transição entre composições, faixas ou fontes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_efeito de \_ tipo \_ principal de linha do tempo**
</dt> <dd>

Objeto Effect. Define um efeito de entrada única a ser aplicado a um objeto composto, de faixa ou de origem.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**LINHA \_ do \_ tipo principal \_ grupo**
</dt> <dd>

Objeto de grupo. Contém uma ou mais faixas de um determinado tipo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj:: gettimelinetype**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




