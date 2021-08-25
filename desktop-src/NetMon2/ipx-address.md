---
description: A estrutura \_ ADDRESS IPX fornece um endereço no nível do protocolo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: IPX_ADDRESS (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0fc8298f2495029d63889fd5ebb24cdb284933897a9d9150b1dfcc2e14084f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743006"
---
# <a name="ipx_address-structure"></a>Estrutura DE \_ ENDEREÇO IPX

A **estrutura \_ ADDRESS IPX** fornece um endereço no nível do protocolo IPX.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sub-rede**
</dt> <dd>

Identificador de sub-rede de rede.

</dd> <dt>

**Endereço**
</dt> <dd>

Identificador de NIC de sub-rede.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




