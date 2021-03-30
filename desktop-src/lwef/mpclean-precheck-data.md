---
title: Estrutura de MPCLEAN_PRECHECK_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada de verificação limpa.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCLEAN_PRECHECK_DATA
- Ponteiro de estrutura de PMPCLEAN_PRECHECK_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454946"
---
# <a name="mpclean_precheck_data-structure"></a>Estrutura de dados de \_ verificação de MPCLEAN \_

Dados de notificação passados para a função de retorno de chamada de verificação limpa.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

Tipo: **\_ informações de PMPRESOURCE**

</dd> <dd>

Informações de recurso sobre o recurso que está sendo bloqueado. Por exemplo, quando o andamento é o **recurso de mpnotify de \_ verificação \_ \_ bloqueado**. Consulte [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**informações de PMPRESOURCE \_**
</dt> <dd>

Tipo: **BlockingResourceInfo**

</dd> <dd>

Informações de recurso sobre o recurso que está bloqueando. Por exemplo, quando o andamento é o **recurso de mpnotify de \_ verificação \_ \_ bloqueado**. Consulte [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> </dl>

 

 





