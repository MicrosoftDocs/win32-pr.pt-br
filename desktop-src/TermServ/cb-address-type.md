---
title: Enumeração de CB_ADDRESS_TYPE (Cbclient. h)
description: Especifica o tipo de endereço.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração de CB_ADDRESS_TYPE
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50903baa9fe85685ef3390ee3d545dd7defff5288d0960d6a2d7ec6ebe2276ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001694"
---
# <a name="cb_address_type-enumeration"></a>Enumeração de tipo de \_ endereço CB \_

Especifica o tipo de endereço.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**\_endereço CB \_ indefinido**
</dt> <dd>

O tipo de endereço é indefinido.

</dd> <dt>

<span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**\_Endereço \_ IPv4 do CB**
</dt> <dd>

O endereço é um endereço IPv4.

</dd> <dt>

<span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**\_IPv6 de endereço CB \_**
</dt> <dd>

O endereço é um endereço IPv6.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



 

 





