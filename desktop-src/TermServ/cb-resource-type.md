---
title: CB_RESOURCE_TYPE enumeração (Cbclient.h)
description: Especifica o tipo de recurso ao qual a conexão de entrada está se conectando.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE enumeração Serviços de Área de Trabalho Remota
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
ms.openlocfilehash: 63dfce0f575147233735dd943645eb51c26141cacaaa61c044698b29b8d118e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139109"
---
# <a name="cb_resource_type-enumeration"></a>\_Enumeração CB RESOURCE \_ TYPE

Especifica o tipo de recurso ao qual a conexão de entrada está se conectando. Essa enumeração é usada com a estrutura [**CB \_ CONNECTION \_ INFO.**](cb-connection-info.md)

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

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB \_ RESOURCE \_ UNDEFINED**
</dt> <dd>

O tipo de recurso não está definido.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB \_ RESOURCE \_ SESSION**
</dt> <dd>

O recurso é uma sessão remota.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_VM DE RECURSO \_ CB**
</dt> <dd>

O recurso é uma máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES \_ DE CONEXÃO \_ CB**](cb-connection-info.md)
</dt> </dl>

 

 





