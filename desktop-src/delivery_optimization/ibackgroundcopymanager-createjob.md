---
title: Método IBackgroundCopyManager CreateJob (Deliveryoptimization.h)
description: Cria um trabalho.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Método CreateJob
- Método CreateJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, método CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165b0a74f71ee5267fb3bd300baec4e48c51662b33c83203ebae1ba462f10a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953556"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>Método IBackgroundCopyManager::CreateJob

Cria um trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDisplayName* \[ Em\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém um nome de exibição para o trabalho. Normalmente, o nome de exibição é usado para identificar o trabalho em uma interface do usuário. Observe que mais de um trabalho pode ter o mesmo nome de exibição. Não deve ser **NULL.** O nome é limitado a 256 caracteres, não incluindo o terminador nulo.

</dd> <dt>

*Tipo* \[ Em\]
</dt> <dd>

Tipo de trabalho de transferência, como BG_JOB_TYPE_DOWNLOAD. Para ver uma lista de tipos de transferência, [**consulte a enumeração BG_JOB_TYPE**](bg-job-type.md) dados.

</dd> <dt>

*pJobID* \[ out\]
</dt> <dd>

Identifica exclusivamente seu trabalho na fila. Use esse identificador ao chamar o [**método IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) para obter um trabalho da fila.

</dd> <dt>

*ppJob* \[ out\]
</dt> <dd>

Um ponteiro de interface [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) que você usa para modificar as propriedades do trabalho e especificar os arquivos a serem transferidos. Para ativar o trabalho na fila, chame o [**método IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md) Libere *ppJob* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                              | Descrição                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | O novo trabalho foi gerado com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Somente o usuário que cria o trabalho ou [](https://www.bing.com/search?q=add+files+to+the+job) um usuário com privilégios de administrador pode adicionar arquivos ao trabalho e alterar as [propriedades do trabalho.](https://www.bing.com/search?q=change+the+job's+properties)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager é definido como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
