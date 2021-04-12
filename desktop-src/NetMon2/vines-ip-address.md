---
description: A estrutura de \_ endereços IP de Vines \_ é um endereço IP em uma rede de Vines.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Estrutura de VINES_IP_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296908"
---
# <a name="vines_ip_address-structure"></a>Estrutura de \_ endereços IP de Vines \_

A estrutura de **\_ \_ endereços IP de Vines** é um endereço IP em uma rede de Vines.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Com e/o**
</dt> <dd>

O identificador de um computador específico em uma sub-rede específica.

</dd> <dt>

**SubnetID**
</dt> <dd>

O identificador de uma sub-rede específica em toda a rede.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




