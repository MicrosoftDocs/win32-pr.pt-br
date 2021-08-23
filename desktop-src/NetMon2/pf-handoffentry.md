---
description: A estrutura de HANDOFFENTRY de PF \_ define um protocolo que monitor de rede adiciona ao conjunto de entrega de um analisador.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Estrutura de PF_HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: faf98490424754d6ae2223ca063e0e3a4eec69c113b1a220e9657b7db5edbb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778666"
---
# <a name="pf_handoffentry-structure"></a>Estrutura de HANDOFFENTRY de PF \_

A estrutura de **\_ HANDOFFENTRY de PF** define um protocolo que monitor de rede adiciona ao conjunto de entrega de um analisador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**szIniFile**
</dt> <dd>

Nome do arquivo INI associado ao protocolo.

</dd> <dt>

**szIniSection**
</dt> <dd>

Rótulo de seção dentro do arquivo INI.

</dd> <dt>

**szProtocol**
</dt> <dd>

Nome do protocolo.

</dd> <dt>

**dwHandOffValue**
</dt> <dd>

Valor associado ao protocolo.

</dd> <dt>

**ValueFormatBase**
</dt> <dd>

A base numérica do valor do protocolo que é especificado em **dwHandOffValue**. A função **ValueFormatBase** deve ser definida como uma das seguintes opções:



| Valor                                                                                                                                                                                                                        | Significado                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**BASE do formato do valor de entrega \_ \_ \_ \_ desconhecida**</dt> </dl> | Base desconhecida<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**\_ \_ decimal base de formato de valor de \_ entrega \_**</dt> </dl> | Base decimal<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**formato de valor de entrega \_ \_ \_ \_ hex base**</dt> </dl>             | Base hexadecimal<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma matriz das estruturas **\_ HANDOFFENTRY do PF** é usada na estrutura [do \_ entregador de PF](pf-handoffset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[teleentregador de PF \_](pf-handoffset.md)
</dt> </dl>

 

 




