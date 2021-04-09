---
description: Contém um número de porta usado para protocolos IP ou IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: União de GENERIC_PORT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920704"
---
# <a name="generic_port-union"></a>\_União de porta genérica

A estrutura de **\_ porta genérica** contém um número de porta usado para protocolos IP ou IPX.

## <a name="syntax"></a>Sintaxe


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a>Membros

<dl> <dt>

**IPPort**
</dt> <dd>

Número da porta IP preenchido.

</dd> <dt>

**ByteSwappedIPXPort**
</dt> <dd>

Número da porta IPX preenchida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




