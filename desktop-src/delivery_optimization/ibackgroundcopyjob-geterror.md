---
title: Método GetError método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera a interface de erro após ocorrer um erro.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Método GetError
- Método GetError, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369616"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>Método método ibackgroundcopyjob:: GetError

Recupera a interface de erro após ocorrer um erro.

A otimização de entrega (DO) gera um objeto de erro quando o estado do trabalho é BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR. O serviço não cria um objeto de erro quando uma chamada para um método de interface **IBackgroundCopyXXXX** falha. O objeto de erro está disponível até que o comece a transferir dados (o estado do trabalho é alterado para BG_JOB_STATE_TRANSFERRING) para o trabalho ou até que o aplicativo saia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppError* \[ fora\]
</dt> <dd>

Interface de erro que fornece o código de erro, uma descrição do erro e o contexto no qual ocorreu o erro. Esse parâmetro também identifica o arquivo que está sendo transferido no momento em que o erro ocorreu. Libere *ppError* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                                                           | Descrição                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                              | Objeto de erro gerado com êxito.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | A interface de erro está disponível somente após ocorrer um erro (BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR) e antes de começar a transferir dados (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Comentários

O trabalho é colocado em um estado de erro em erros fatais. Use uma das opções a seguir para determinar se o trabalho está em erro:

-   Para sondar o estado do trabalho, chame o método [**método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) . O trabalho estará em erro se o estado for BG_JOB_STATE_ERROR.
-   Para receber uma notificação quando ocorrer um erro, implemente a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (especificamente, o método [**JobError**](https://www.bing.com/search?q=**JobError**) ). Em seguida, chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para registrar o retorno de chamada e o método [**método ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para definir o sinalizador de BG_NOTIFY_JOB_ERROR.

A interface [**IBackgroundCopyError**](ibackgroundcopyerror.md) contém informações que você usa para determinar a causa do erro e se o processo de transferência pode continuar. Depois de determinar a causa do erro, execute uma das seguintes opções:

-   Para cancelar o trabalho, chame o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Para salvar os arquivos transferidos com êxito antes da ocorrência do erro, chame o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .
-   Para concluir o processamento do trabalho, corrija o problema e, em seguida, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) .

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

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





