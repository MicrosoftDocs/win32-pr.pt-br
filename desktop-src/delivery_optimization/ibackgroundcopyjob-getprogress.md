---
title: Método GetProgress de IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Método GetProgress
- Método GetProgress, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07a498aef2a9dcfd108733b45526bd876817d8d5075323d0edd95c7cbf3de8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755316"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a>Método IBackgroundCopyJob::GetProgress

Recupera informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProgress* \[ out\]
</dt> <dd>

Contém dados que você pode usar para calcular o percentual do trabalho concluído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                              | Descrição                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | As informações de progresso foram recuperadas com êxito.<br/> |



 

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
</dt> </dl>

 

 





