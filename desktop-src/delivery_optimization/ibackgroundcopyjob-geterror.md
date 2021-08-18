---
title: Método GetError IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera a interface de erro depois que ocorre um erro.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Método GetError
- Método GetError, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método GetError
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
ms.openlocfilehash: 016f11023d50d7ea1fa9024e270a7ebce0597e07d5c33a915facae47773759c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755506"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>Método IBackgroundCopyJob::GetError

Recupera a interface de erro depois que ocorre um erro.

Otimização de Entrega (DO) gera um objeto de erro quando o estado do trabalho é BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR. O serviço não cria um objeto de erro quando uma chamada para um método de interface **IBackgroundCopyXXXX** falha. O objeto de erro está disponível até que DO comece a transferir dados (o estado do trabalho muda para BG_JOB_STATE_TRANSFERRING) para o trabalho ou até que o aplicativo seja finalado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppError* \[ out\]
</dt> <dd>

Interface de erro que fornece o código de erro, uma descrição do erro e o contexto no qual o erro ocorreu. Esse parâmetro também identifica o arquivo que está sendo transferido no momento em que o erro ocorreu. Libere *ppError* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                                                           | Descrição                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>                              | O objeto de erro foi gerado com êxito.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | A interface de erro está disponível somente depois que ocorre um erro (BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR) e antes que o DO comece a transferir dados (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Comentários

O trabalho é colocado em um estado de erro em erros fatais. Use uma das seguintes opções para determinar se o trabalho está com erro:

-   Para sondar o estado do trabalho, chame o [**método IBackgroundCopyJob::GetState.**](ibackgroundcopyjob-getstate.md) O trabalho está em erro se o estado for BG_JOB_STATE_ERROR.
-   Para receber notificação quando ocorrer um erro, implemente a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (especificamente, o [**método JobError).**](https://www.bing.com/search?q=**JobError**) Em seguida, chame o método [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para registrar o retorno de chamada e o método [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para definir o sinalizador BG_NOTIFY_JOB_ERROR.

A interface [**IBackgroundCopyError**](ibackgroundcopyerror.md) contém informações que você usa para determinar a causa do erro e se o processo de transferência pode continuar. Depois de determinar a causa do erro, execute uma das seguintes opções:

-   Para cancelar o trabalho, chame o [**método IBackgroundCopyJob::Cancel.**](ibackgroundcopyjob-cancel.md)
-   Para salvar os arquivos transferidos com êxito antes do erro, chame o [**método IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md)
-   Para concluir o processamento do trabalho, corrige o problema e chame o [**método IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md)

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

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





