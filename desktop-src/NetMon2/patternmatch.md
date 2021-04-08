---
description: A estrutura PATTERNMATCH define os elementos de padrão usados para avaliar um quadro.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Estrutura PATTERNMATCH (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922003"
---
# <a name="patternmatch-structure"></a>Estrutura PATTERNMATCH

A estrutura **PATTERNMATCH** define os elementos de padrão usados para avaliar um quadro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sinalizadores**
</dt> <dd>

Sinalizadores de correspondência de padrões:



| Valor                                                                                                                                                                                                                                                                                           | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <dt>**Padrão \_ Sinalizadores de correspondência \_ \_ não**</dt> <dt>0x00000001</dt> </dl>                                   | Quando definido, esse sinalizador retém os quadros que não têm o padrão especificado no ponto adequado.<br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <dt>**Padrão \_ Porta de sinalizadores de correspondência \_ \_ \_ especificada**</dt> <dt>0x00000008</dt> </dl> | Busca um valor de número de porta.<br/>                                                             |



 

</dd> <dt>

**OffsetBasis**
</dt> <dd>

Tipos de deslocamento, que podem ser um dos seguintes:



| Valor                                                                                                                                                                                                                                                       | Significado                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <dt>**DESLOCAMENTO \_ \_ de base relativo \_ ao \_ quadro**</dt> </dl>                                         | Define um deslocamento, em bytes, em relação ao início do quadro.<br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <dt>**DESLOCAMENTO \_ \_ de base \_ relativo \_ ao \_ protocolo efetivo**</dt> </dl> | Define um deslocamento, em bytes, em relação ao início do protocolo referenciado.<br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <dt>**DESLOCAMENTO \_ \_ de base relativo \_ ao \_ IPX**</dt> </dl>                                               | Define um deslocamento, em bytes, somente relativo ao IPX.<br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <dt>**DESLOCAMENTO \_ \_ de base relativo \_ ao \_ IP**</dt> </dl>                                                  | Define um deslocamento, em bytes, somente relativo ao IP.<br/>                              |



 

</dd> <dt>

**Porta**
</dt> <dd>

Valor da porta, se especificado.

</dd> <dt>

**Deslocamento**
</dt> <dd>

O deslocamento, em bytes, relativo ao **OffsetBasis**.

</dd> <dt>

**Comprimento**
</dt> <dd>

Comprimento do padrão correspondente.

</dd> <dt>

**PatternToMatch**
</dt> <dd>

Padrão a ser correspondido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada para construir um filtro de captura. Para obter mais informações sobre como implementar essa estrutura, consulte [filtros de captura](capture-filters.md).

Um filtro de captura pode conter até quatro estruturas **PATTERNMATCH** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




