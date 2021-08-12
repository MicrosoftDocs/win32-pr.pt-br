---
title: Método método ibackgroundcopyjob SetNotifyFlags (Deliveryoptimization. h)
description: Especifica o tipo de notificação de evento que você deseja receber, como eventos de transferência de trabalho.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Método SetNotifyFlags
- Método SetNotifyFlags, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método SetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdb1750391027163a7ac8fb9ba8cc20085a06d187de0d7f05850641a5a774b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542913"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a>Método método ibackgroundcopyjob:: SetNotifyFlags

Especifica o tipo de notificação de evento que você deseja receber, como eventos de transferência de trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NotifyFlags* \[ no\]
</dt> <dd>

Defina um ou mais dos sinalizadores a seguir para identificar os eventos que você deseja receber.



| Valor                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt> </dl>                          | Todos os arquivos no trabalho foram transferidos.<br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt> </dl>                                            | Ocorreu um erro.<br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt> </dl>                                                   | Sem suporte.<br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt> </dl>                       | O trabalho foi modificado. Por exemplo, um valor de propriedade alterado, o estado do trabalho foi alterado ou o progresso é feito transferindo os arquivos. Esse sinalizador será ignorado se a notificação de linha de comando for especificada.<br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt> </dl>                       | Um arquivo no trabalho foi transferido. Esse sinalizador será ignorado se a notificação de linha de comando for especificada.<br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt> </dl> | Sem suporte.<br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                                          | Descrição                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | O tipo de notificação de eventos foi definido com êxito.<br/>                                          |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentários

Use o método **SetNotifyFlags** em conjunto com [**método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





