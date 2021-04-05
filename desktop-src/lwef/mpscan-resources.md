---
title: Estrutura de MPSCAN_RESOURCES (MpClient. h)
description: Informações de recurso passadas durante uma operação de verificação.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSCAN_RESOURCES
- Ponteiro de estrutura de PMPSCAN_RESOURCES recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919176"
---
# <a name="mpscan_resources-structure"></a>\_Estrutura de recursos MPSCAN

Informações de recurso passadas durante uma operação de verificação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Contagem de recursos.

</dd> <dt>

**origem**
</dt> <dd>

Tipo: **\_ informações de PMPRESOURCE**

</dd> <dd>

Matriz de recursos. Consulte [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> </dl>

 

 





