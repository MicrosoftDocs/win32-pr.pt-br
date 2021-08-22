---
title: Método GetId IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera o identificador usado para identificar o trabalho na fila.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- Método GetId
- Método GetId, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01c696985b4b632223318675fd63f842b85ed6e27297ff1befebbac1b3fa9bce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755496"
---
# <a name="ibackgroundcopyjobgetid-method"></a>Método IBackgroundCopyJob::GetId

Recupera o identificador usado para identificar o trabalho na fila.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJobID* \[ out\]
</dt> <dd>

GUID que identifica o trabalho dentro da fila do DO.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão do COM **HRESULT** em caso de erro.

## <a name="remarks"></a>Comentários

O serviço gera o identificador quando você [cria](ibackgroundcopymanager-createjob.md) o trabalho. Para usar o identificador para recuperar um ponteiro de interface [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) para o trabalho, chame o [**método IBackgroundCopyManager::GetJob.**](ibackgroundcopymanager-getjob.md)

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

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





