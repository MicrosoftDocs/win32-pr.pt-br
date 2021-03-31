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
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644421"
---
# <a name="cb_address_type-enumeration"></a>Enumeração de tipo de \_ endereço CB \_

Especifica o tipo de endereço.

## <a name="syntax"></a>Sintaxe


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
| parâmetro<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



 

 





