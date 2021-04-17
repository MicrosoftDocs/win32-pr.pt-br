---
title: Método IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: A otimização de entrega (DO) chama a implementação do método JobError quando o estado do trabalho é alterado para BG_JOB_STATE_ERROR.
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
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369545"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>Método IBackgroundCopyCallback:: JobError

A otimização de entrega (DO) chama a implementação do método [**JobError**](https://www.bing.com/search?q=**JobError**) quando o estado do trabalho é alterado para BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJob* \[ no\]
</dt> <dd>

Contém informações relacionadas ao trabalho, como o número de bytes e arquivos transferidos antes de o erro ter ocorrido. Ele também contém os métodos para retomar e cancelar o trabalho. Não liberar *pJob*; Libera a interface quando o método [**JobError**](https://www.bing.com/search?q=**JobError**) retorna.

</dd> <dt>

*perror* \[ no\]
</dt> <dd>

Contém informações de erro, como o arquivo que está sendo processado no momento em que ocorreu o erro fatal e uma descrição do erro. Não liberar *perror*; Libera a interface quando o método [**JobError**](https://www.bing.com/search?q=**JobError**) retorna.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Este método deve retornar **S_OK**; caso contrário, o continuará a chamar esse método até que **S_OK** seja retornado. Por motivos de desempenho, você deve limitar o número de vezes que retorna um valor diferente de **S_OK** a algumas vezes. Como alternativa para retornar um código de erro, considere sempre retornar **S_OK** e manipular o erro internamente. O intervalo no qual esse método é chamado é arbitrário.

## <a name="remarks"></a>Comentários

Depois de determinar a causa do erro, execute uma das seguintes opções:

-   Para cancelar o trabalho, chame o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Para aceitar a parte do trabalho que foi transferida com êxito antes da ocorrência do erro, chame o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) . Esta opção não se aplica aos trabalhos de carregamento; Não é possível concluir uma parte de um trabalho de carregamento.
-   Para concluir o processamento do trabalho, corrija o problema e, em seguida, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) .

Os erros transitórios não geram chamadas para o método [**JobError**](https://www.bing.com/search?q=**JobError**) .

O retorna BG_ERROR_CONTEXT_REMOTE_FILE se o trabalho atingir um erro HTTP 403, BG_ERROR_CONTEXT_NONE caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: retomar**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





