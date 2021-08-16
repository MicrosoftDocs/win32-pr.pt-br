---
title: Método IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Recupera um trabalho especificado da fila de transferência. Normalmente, seu aplicativo persiste o identificador de trabalho, para que você possa recuperar posteriormente o trabalho da fila.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Método GetJob
- Método GetJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, método GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d8d05b496eaa0d6f1520f22efeed8a39af5eb8e4c338457e18c65a7913489472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542284"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>Método IBackgroundCopyManager:: GetJob

Recupera um trabalho especificado da fila de transferência. Normalmente, seu aplicativo persiste o identificador de trabalho, para que você possa recuperar posteriormente o trabalho da fila.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*JobID* \[ no\]
</dt> <dd>

Identifica o trabalho a ser recuperado da fila de transferência. O método [**CreateJob**](ibackgroundcopymanager-createjob.md) retorna o identificador do trabalho.

</dd> <dt>

*ppJob* \[ fora\]
</dt> <dd>

Um ponteiro de interface [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md) para o trabalho especificado por *JobID*. Quando terminar, libere *ppJob*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                                      | Descrição                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>         | O trabalho foi recuperado com êxito da fila de transferência.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | O trabalho não foi encontrado na fila.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | O usuário não tem permissão para recuperar o trabalho.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager é definido como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





