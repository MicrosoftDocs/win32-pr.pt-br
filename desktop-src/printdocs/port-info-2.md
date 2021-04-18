---
description: A \_ estrutura informações sobre a porta \_ 2 identifica uma porta de impressora com suporte.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Estrutura de PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813983"
---
# <a name="port_info_2-structure"></a>Estrutura de informações da porta \_ \_ 2

A **estrutura \_ informações \_ sobre a porta 2** identifica uma porta de impressora com suporte.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**pPortName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que identifica uma porta de impressora com suporte (por exemplo, "LPT1:").

</dd> <dt>

**pMonitorName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que identifica um monitor instalado (por exemplo, "Monitor de PJL"). Isso pode ser **nulo**.

</dd> <dt>

**pDescription**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que descreve a porta com mais detalhes (por exemplo, se **pPortName** for "LPT1:", **pDescription** é "porta da impressora"). Isso pode ser **nulo**.

</dd> <dt>

**fPortType**
</dt> <dd>

Bitmask que descreve o tipo de porta. Esse membro pode ser uma combinação dos seguintes valores:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**\_gravação de tipo de porta \_**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**\_leitura do tipo de porta \_**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**tipo de porta \_ \_ Redirecionado**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**tipo de porta \_ \_ rede \_ anexada**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reservado deve ser zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use a **estrutura \_ informações \_ da porta 2** ao chamar [**EnumPorts**](enumports.md) se houver vários monitores instalados que ofereçam suporte às mesmas portas.

O membro **fPortType** pode ser consultado para determinar informações sobre a porta. Observe que as configurações de porta não influenciam os atributos da impressora (como retornado pelo membro **Attributes** das [**informações da impressora \_ \_ 2**](printer-info-2.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de porta **\_ \_ \_ 2W** (Unicode) e **\_ informação de porta \_ \_ 2a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




