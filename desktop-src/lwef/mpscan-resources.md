---
title: MPSCAN_RESOURCES estrutura (MpClient.h)
description: Informações de recurso passadas durante uma operação de verificação.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES estrutura herdada Windows recursos de ambiente
- PMPSCAN_RESOURCES de estrutura herdado Windows recursos de ambiente
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
ms.openlocfilehash: dd70b442e7179d516d2e9c60b81e6c52b0f696f5719a255871e8687773bf71ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747345"
---
# <a name="mpscan_resources-structure"></a>Estrutura DE RECURSOS DO MPSCAN \_

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

**pResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Matriz de recursos. Consulte [**INFORMAÇÕES DO MPRESOURCE. \_**](mpresource-info.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DO MPRESOURCE \_**](mpresource-info.md)
</dt> </dl>

 

 





