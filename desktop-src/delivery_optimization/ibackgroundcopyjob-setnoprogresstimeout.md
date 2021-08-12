---
title: Método método ibackgroundcopyjob SetNoProgressTimeout (Deliveryoptimization. h)
description: Define o período de tempo que a otimização de entrega (DO) tenta transferir o arquivo depois que ocorre uma condição de erro transitória. Se houver um progresso, o temporizador será redefinido.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Método SetNoProgressTimeout
- Método SetNoProgressTimeout, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método SetNoProgressTimeout
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
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>Método método ibackgroundcopyjob:: SetNoProgressTimeout

Define o período de tempo que a otimização de entrega (DO) tenta transferir o arquivo depois que ocorre uma condição de erro transitória. Se houver um progresso, o temporizador será redefinido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RetryPeriod* \[ no\]
</dt> <dd>

Período de tempo, em segundos, que tenta transferir o arquivo após não ter sido feito nenhum progresso. O período de repetição padrão para trabalho de alta prioridade é de 3600 segundos (1 hora) e o trabalho de baixa prioridade é de 86400 segundos (24 horas).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                                          | Descrição                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Período de repetição definido com êxito.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentários

Se o não fizer o andamento durante o período de repetição, ele moverá o estado do trabalho de BG_JOB_STATE_TRANSIENT_ERROR para BG_JOB_STATE_ERROR. Se você solicitar uma notificação de erro, o chamará o retorno de chamada [**JobError**](https://www.bing.com/search?q=**JobError**) .

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

[**Método ibackgroundcopyjob:: GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





