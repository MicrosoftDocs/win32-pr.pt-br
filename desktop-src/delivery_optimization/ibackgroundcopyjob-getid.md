---
title: Método método ibackgroundcopyjob GetId (Deliveryoptimization. h)
description: Recupera o identificador usado para identificar o trabalho na fila.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- Método GetId
- Método GetId, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetId
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
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105807180"
---
# <a name="ibackgroundcopyjobgetid-method"></a>Método método ibackgroundcopyjob:: GetId

Recupera o identificador usado para identificar o trabalho na fila.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJobID* \[ fora\]
</dt> <dd>

O GUID que identifica o trabalho dentro da fila do.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.

## <a name="remarks"></a>Comentários

O serviço gera o identificador quando você [cria](ibackgroundcopymanager-createjob.md) o trabalho. Para usar o identificador para recuperar um ponteiro de interface [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md) para o trabalho, chame o método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .

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

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





