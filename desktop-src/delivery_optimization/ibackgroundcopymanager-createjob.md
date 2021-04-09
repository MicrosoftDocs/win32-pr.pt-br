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
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/27/2021
ms.locfileid: "104011881"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>Método IBackgroundCopyManager:: CreateJob

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

*pDisplayName* \[ no\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém um nome de exibição para o trabalho. Normalmente, o nome de exibição é usado para identificar o trabalho em uma interface do usuário. Observe que mais de um trabalho pode ter o mesmo nome de exibição. Não deve ser **nulo**. O nome é limitado a 256 caracteres, não incluindo o terminador nulo.

</dd> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Tipo de trabalho de transferência, como BG_JOB_TYPE_DOWNLOAD. Para obter uma lista de tipos de transferência, consulte a enumeração [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> <dt>

*pJobID* \[ fora\]
</dt> <dd>

Identifica exclusivamente seu trabalho na fila. Use esse identificador ao chamar o método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) para obter um trabalho da fila.

</dd> <dt>

*ppJob* \[ fora\]
</dt> <dd>

Um ponteiro de interface [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md) que você usa para modificar as propriedades do trabalho e especificar os arquivos a serem transferidos. Para ativar o trabalho na fila, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) . Libere *ppJob* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Novo trabalho gerado com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Somente o usuário que cria o trabalho ou um usuário com privilégios de administrador pode [Adicionar arquivos ao trabalho](https://www.bing.com/search?q=add+files+to+the+job) e [alterar as propriedades do trabalho](https://www.bing.com/search?q=change+the+job's+properties).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager é definido como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: retomar**](ibackgroundcopyjob-resume.md)
</dt> </dl>
