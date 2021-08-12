---
title: Método Suspend IBackgroundCopyJob (Deliveryoptimization.h)
description: Suspende um trabalho. Novos trabalhos, trabalhos que estão com erros e trabalhos que finalizaram a transferência de arquivos são suspensos automaticamente.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Método Suspend
- Método Suspend, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método Suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9458347c8f09a2f04c4e2800a0f2f747571f5519b322133ef4b874b15cf77a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542805"
---
# <a name="ibackgroundcopyjobsuspend-method"></a>Método IBackgroundCopyJob::Suspend

Suspende um trabalho. Novos trabalhos, trabalhos que estão com erros e trabalhos que finalizaram a transferência de arquivos são suspensos automaticamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Suspend();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                                          | Descrição                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | O trabalho foi suspenso com êxito.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





