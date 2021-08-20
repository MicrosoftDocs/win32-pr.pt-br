---
title: Método IBackgroundCopyJob SetNoProgressTimeout (Deliveryoptimization.h)
description: Define o período de tempo que Otimização de Entrega (DO) tenta transferir o arquivo depois que ocorre uma condição de erro transitório. Se houver progresso, o temporizador será redefinido.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Método SetNoProgressTimeout
- Método SetNoProgressTimeout, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcf6905388d54103aaac34ae934c89e2fd8ccc16ce32a384eb730376606351b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542923"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>Método IBackgroundCopyJob::SetNoProgressTimeout

Define o período de tempo que Otimização de Entrega (DO) tenta transferir o arquivo depois que ocorre uma condição de erro transitório. Se houver progresso, o temporizador será redefinido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RetryPeriod* \[ Em\]
</dt> <dd>

Período de tempo, em segundos, que o DO tenta transferir o arquivo depois que não houve nenhum progresso. O período de repetir padrão para o trabalho de alta prioridade é de 3600 segundos (1 hora) e para o trabalho de baixa prioridade é de 86400 segundos (24 horas).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                                          | Descrição                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | Período de tentativa definido com êxito.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentários

Se o DO não fizer progresso durante o período de tentativa, ele move o estado do trabalho de BG_JOB_STATE_TRANSIENT_ERROR para BG_JOB_STATE_ERROR. Se você solicitar notificação de erro, DO chamará o retorno [**de chamada JobError.**](https://www.bing.com/search?q=**JobError**)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





