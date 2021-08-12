---
title: Método JobError IBackgroundCopyCallback (Deliveryoptimization.h)
description: Otimização de Entrega (DO) chama sua implementação do método JobError quando o estado do trabalho muda para BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Método JobError
- Método JobError, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, método JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 307ab18a0f956e5a2f4f14e9782f90b8ec6bff723da04aa9866566d95c53dca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543128"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>Método IBackgroundCopyCallback::JobError

Otimização de Entrega (DO) chama sua implementação do método [**JobError**](https://www.bing.com/search?q=**JobError**) quando o estado do trabalho muda para BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJob* \[ Em\]
</dt> <dd>

Contém informações relacionadas ao trabalho, como o número de bytes e arquivos transferidos antes do erro. Ele também contém os métodos para retomar e cancelar o trabalho. Não libere *pJob*; O DO libera a interface quando o [**método JobError**](https://www.bing.com/search?q=**JobError**) retorna.

</dd> <dt>

*pError* \[ Em\]
</dt> <dd>

Contém informações de erro, como o arquivo que está sendo processado no momento em que o erro fatal ocorreu e uma descrição do erro. Não libere *pError*; O DO libera a interface quando o [**método JobError**](https://www.bing.com/search?q=**JobError**) retorna.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método deve retornar **S_OK**; caso contrário, DO continuará a chamar esse método **até que S_OK** seja retornado. Por motivos de desempenho, você deve limitar o número de vezes que retorna um valor diferente **S_OK** a algumas vezes. Como alternativa ao retorno de um código de erro, considere sempre retornar S_OK **e** tratar o erro internamente. O intervalo no qual esse método é chamado é arbitrário.

## <a name="remarks"></a>Comentários

Depois de determinar a causa do erro, execute uma das seguintes opções:

-   Para cancelar o trabalho, chame o [**método IBackgroundCopyJob::Cancel.**](ibackgroundcopyjob-cancel.md)
-   Para aceitar a parte do trabalho que foi transferida com êxito antes do erro, chame o [**método IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md) Essa opção não se aplica a trabalhos de upload; você não pode concluir uma parte de um trabalho de upload.
-   Para concluir o processamento do trabalho, corrige o problema e chame o [**método IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md)

Erros transitórios não geram chamadas para o [**método JobError.**](https://www.bing.com/search?q=**JobError**)

DO retornará BG_ERROR_CONTEXT_REMOTE_FILE se o trabalho tiver atingido um erro HTTP 403, caso BG_ERROR_CONTEXT_NONE contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





