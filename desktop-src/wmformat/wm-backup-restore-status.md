---
title: Estrutura de WM_BACKUP_RESTORE_STATUS (wmdrmsdk. h)
description: A estrutura de status de restauração de backup do WM \_ \_ \_ contém informações sobre uma operação de backup ou restauração de licença pendente.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Formato de mídia do Windows de estrutura de WM_BACKUP_RESTORE_STATUS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811639"
---
# <a name="wm_backup_restore_status-structure"></a>\_Estrutura de \_ status de restauração de backup do WM \_

A estrutura de status de restauração de backup do WM contém informações sobre uma operação de backup ou restauração de licença pendente. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**eStatus**
</dt> <dd>

Membro da enumeração [**de \_ status Msdrm**](msdrm-status.md) especificando o status.

</dd> <dt>

**bstrError**
</dt> <dd>

Cadeia de caracteres que contém o erro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é recebida quando você chama o método [**IWMDRMLicenseBackupRestoreStatus:: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) . Ele contém o status da operação pendente de backup ou restauração no momento da chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





