---
title: Método GetStatus IWMDRMLicenseBackupRestoreStatus (wmdrmsdk. h)
description: O método GetStatus recupera informações detalhadas de status sobre uma operação de backup ou restauração de licença.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Método GetStatus Windows Media Format
- Método GetStatus Windows Media Format, interface IWMDRMLicenseBackupRestoreStatus
- Formato de mídia do Windows da interface IWMDRMLicenseBackupRestoreStatus, método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0646a1fd5caaa898ede1afb3d09b54ff3d455a809a10a9b37fa0f9d8ab2aba91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655164"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>Método IWMDRMLicenseBackupRestoreStatus:: GetStatus

O método **GetStatus** recupera informações detalhadas de status sobre uma operação de backup ou restauração de licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStatus* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura de status de restauração de backup do WM que recebe as informações de status. [**\_ \_ \_**](wm-backup-restore-status.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





