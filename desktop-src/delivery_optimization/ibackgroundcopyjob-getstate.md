---
title: Método GetState método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera o estado do trabalho.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Método GetState
- Método GetState, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644704"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>Método método ibackgroundcopyjob:: GetState

Recupera o estado do trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJobState* \[ fora\]
</dt> <dd>

O estado do trabalho. Por exemplo, o estado reflete se o trabalho está em erro, transferindo dados ou suspenso. Para obter uma lista de Estados de trabalho, consulte a enumeração [**BG_JOB_STATE**](bg-job-state-.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | O estado do trabalho foi recuperado com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Se você quiser saber quando um trabalho está com erro ou transferiu todos os arquivos do trabalho, você pode usar esse método para sondar o estado do trabalho ou pode se registrar para receber notificações quando ocorrerem eventos. Para obter detalhes sobre como registrar-se para receber a notificação de eventos, consulte a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





