---
title: Método método ibackgroundcopyjob GetNotifyInterface (Deliveryoptimization. h)
description: Recupera o ponteiro de interface para sua implementação da interface IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Método GetNotifyInterface
- Método GetNotifyInterface, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763801"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a>Método método ibackgroundcopyjob:: GetNotifyInterface

Recupera o ponteiro de interface para sua implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppNotifyInterface* \[ fora\]
</dt> <dd>

Ponteiro de interface para sua implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Quando terminar, libere *ppNotifyInterface*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | O ponteiro da interface de notificação foi recuperado com êxito.<br/> |



 

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





