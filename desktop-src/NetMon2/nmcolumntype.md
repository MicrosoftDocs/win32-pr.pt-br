---
description: Especifica os membros da estrutura NMCOLUMNVARIANT.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Enumeração NMCOLUMNTYPE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5e3877a15a55ac1d942a068843173e2771202047691f3df96601fe4b9de3152a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799496"
---
# <a name="nmcolumntype-enumeration"></a>Enumeração NMCOLUMNTYPE

A **enumeração NMCOLUMNTYPE** especifica os membros da [**estrutura NMCOLUMNVARIANT.**](nmcolumnvariant.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE \_ UINT8**
</dt> <dd>

Inteiro sem sinal de 8 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE \_ SINT8**
</dt> <dd>

Inteiro com sinal de 8 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UINT16**
</dt> <dd>

Inteiro sem sinal de 16 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE \_ SINT16**
</dt> <dd>

Inteiro com sinal de 16 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE \_ UINT32**
</dt> <dd>

Inteiro sem sinal de 32 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE \_ SINT32**
</dt> <dd>

Inteiro com sinal de 32 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE \_ FLOAT64**
</dt> <dd>

Float de 64 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**QUADRO NMCOLUMNTYPE \_**
</dt> <dd>

Número do quadro.

</dd> <dt>

<span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE \_ YESNO**
</dt> <dd>

"Sim" ou "Não".

</dd> <dt>

<span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE \_ ONOFF**
</dt> <dd>

"On" ou "Off"

</dd> <dt>

<span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE \_ TRUEFALSE**
</dt> <dd>

"True" ou "False".

</dd> <dt>

<span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE \_ MACADDR**
</dt> <dd>

Endereço MAC.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE \_ IPXADDR**
</dt> <dd>

Endereço IPX.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE \_ IPADDR**
</dt> <dd>

Endereço IP.

</dd> <dt>

<span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE \_ VARTIME**
</dt> <dd>

Hora da variante.

</dd> <dt>

<span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**CADEIA DE CARACTERES NMCOLUMNTYPE \_**
</dt> <dd>

Ponteiro para uma cadeia de caracteres.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




