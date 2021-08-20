---
title: WM_BACKUP_RESTORE_STATUS estrutura (Wmdrmsdk.h)
description: A estrutura WM BACKUP RESTORE STATUS contém informações sobre uma operação de backup ou restauração de \_ \_ licença \_ pendente.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- WM_BACKUP_RESTORE_STATUS formato de mídia do Windows
- formato de mídia de janelas de estrutura
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
ms.openlocfilehash: a7f7d67cc67d6d983cf412a0bea82d26ad748da87ba770373554a15826c983ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118028311"
---
# <a name="wm_backup_restore_status-structure"></a>Estrutura WM \_ BACKUP \_ RESTORE \_ STATUS

A **estrutura WM BACKUP RESTORE \_ \_ \_ STATUS** contém informações sobre uma operação de backup ou restauração de licença pendente.

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

Membro da [**enumeração \_ STATUS do MSDRM**](msdrm-status.md) especificando o status.

</dd> <dt>

**bstrError**
</dt> <dd>

Cadeia de caracteres que contém o erro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é recebida quando você chama o [**método IWMDRMLicenseBackupRestoreStatus::GetStatus.**](iwmdrmlicensebackuprestorestatus-getstatus.md) Ele contém o status da operação de backup ou restauração pendente no momento da chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





