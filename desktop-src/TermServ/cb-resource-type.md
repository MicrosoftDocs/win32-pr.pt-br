---
title: Enumeração de CB_RESOURCE_TYPE (Cbclient. h)
description: Especifica o tipo de recurso ao qual a conexão de entrada está se conectando.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração de CB_RESOURCE_TYPE
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644420"
---
# <a name="cb_resource_type-enumeration"></a>Enumeração de tipo de \_ recurso CB \_

Especifica o tipo de recurso ao qual a conexão de entrada está se conectando. Essa enumeração é usada com a estrutura de [**\_ \_ informações de conexão CB**](cb-connection-info.md) .

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**\_recurso CB \_ indefinido**
</dt> <dd>

O tipo de recurso não está definido.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_sessão de recurso CB \_**
</dt> <dd>

O recurso é uma sessão remota.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_VM de recurso CB \_**
</dt> <dd>

O recurso é uma máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de conexão CB \_**](cb-connection-info.md)
</dt> </dl>

 

 





