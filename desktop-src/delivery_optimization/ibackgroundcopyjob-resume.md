---
title: Método de retomada método ibackgroundcopyjob (Deliveryoptimization. h)
description: Ativa um novo trabalho ou reinicia um trabalho que foi suspenso.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Método Resume
- Método resume, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa4bd9a98626b7f26fc4ac9968d27d54604b5db56539eb383bb8aff696b2a561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543002"
---
# <a name="ibackgroundcopyjobresume-method"></a>Método método ibackgroundcopyjob:: resume

Ativa um novo trabalho ou reinicia um trabalho que foi suspenso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                                          | Descrição                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | O trabalho foi reiniciado com êxito.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | Não existem arquivos a transferir.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentários

Quando você cria um trabalho, o trabalho é suspenso inicialmente. Chamar **resume** move o trabalho para o estado de transferência. Observe que o trabalho deve conter um ou mais arquivos antes de chamar esse método.

Se um trabalho que está no estado BG_JOB_STATE_TRANSIENT_ERROR ou BG_JOB_STATE_ERROR, chame o método **resume** para reiniciar o trabalho depois de corrigir o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: suspender**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





