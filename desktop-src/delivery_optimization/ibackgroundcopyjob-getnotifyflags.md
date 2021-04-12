---
title: Método método ibackgroundcopyjob GetNotifyFlags (Deliveryoptimization. h)
description: Recupera os sinalizadores de notificação de eventos para o trabalho.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Método GetNotifyFlags
- Método GetNotifyFlags, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295783"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a>Método método ibackgroundcopyjob:: GetNotifyFlags

Recupera os sinalizadores de notificação de eventos para o trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNotifyFlags* \[ fora\]
</dt> <dd>

Identifica os eventos que seu aplicativo recebe. A tabela a seguir lista os valores de sinalizador de notificação de eventos.



| Valor                                                                                                                                                                                                  | Significado                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> </dl>    | Todos os arquivos no trabalho foram transferidos.<br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> </dl>                      | Ocorreu um erro.<br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> </dl>                             | A notificação de eventos está desabilitada. Se definido, ignora os outros sinalizadores.<br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> </dl> | O trabalho foi modificado.<br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Os sinalizadores de notificação de eventos foram recuperados com êxito.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
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

[**Método ibackgroundcopyjob:: GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





