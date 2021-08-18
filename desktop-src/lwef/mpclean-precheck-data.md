---
title: Estrutura de MPCLEAN_PRECHECK_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada de verificação limpa.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPCLEAN_PRECHECK_DATA
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPCLEAN_PRECHECK_DATA
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
ms.openlocfilehash: bc272ed230a67811497f0eebb99624d74369c8c55419fba970f326fba502e8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747922"
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> </dl>

 

 





