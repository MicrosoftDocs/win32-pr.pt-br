---
description: A estrutura PORT \_ INFO \_ 2 identifica uma porta de impressora com suporte.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: PORT_INFO_2 (Winspool.h)
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
ms.openlocfilehash: 053745ff90e022ef2ed466518a9210d6dde18d3562fdb4232d9f4d262460ea7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470936"
---
# <a name="port_info_2-structure"></a>Estrutura PORT \_ INFO \_ 2

A **estrutura PORT INFO \_ \_ 2** identifica uma porta de impressora com suporte.

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

Ponteiro para uma cadeia de caracteres terminada em nulo que identifica um monitor instalado (por exemplo, "Monitor PJL"). Pode ser **NULL.**

</dd> <dt>

**pDescription**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que descreve a porta mais detalhadamente (por exemplo, se **pPortName** for "LPT1:", **pDescription** será "porta de impressora"). Pode ser **NULL.**

</dd> <dt>

**fPortType**
</dt> <dd>

Bitmask que descreve o tipo de porta. Esse membro pode ser uma combinação dos seguintes valores:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**GRAVAÇÃO \_ DE TIPO DE \_ PORTA**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**LEITURA \_ DE TIPO DE \_ PORTA**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**TIPO \_ DE PORTA \_ REDIRECIONADO**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**TIPO \_ DE PORTA NET \_ \_ ANEXADO**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reservado; deve ser zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use a **estrutura PORT \_ INFO \_ 2** ao chamar [**EnumPorts**](enumports.md) se houver vários monitores instalados que deem suporte às mesmas portas.

O **membro fPortType** pode ser consultado para determinar informações sobre a porta. Observe que as configurações de porta não influenciam os atributos da impressora (conforme retornado pelo membro **Atributos** do [**PRINTER INFO \_ \_ 2**](printer-info-2.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ PORT \_ INFO \_ 2W** (Unicode) e **\_ PORT INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




