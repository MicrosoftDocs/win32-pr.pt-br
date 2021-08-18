---
title: Método GetTimes IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera carimbos de data/hora relacionados ao trabalho, como a hora em que o trabalho foi criado ou modificado pela última vez.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Método GetTimes
- Método GetTimes, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método GetTimes
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3179342630fe932dd55efc4e75e15cd06a879d6cdc93005981cc7e0ebca7e05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755206"
---
# <a name="ibackgroundcopyjobgettimes-method"></a>Método IBackgroundCopyJob::GetTimes

Recupera carimbos de data/hora relacionados ao trabalho, como a hora em que o trabalho foi criado ou modificado pela última vez.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimes* \[ out\]
</dt> <dd>

Contém carimbos de data/hora relacionados ao trabalho. Para ver os carimbos de data/hora disponíveis, consulte a [**estrutura BG_JOB_TIMES**](bg-job-times.md) dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                              | Descrição                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Os carimbos de data/hora foram recuperados com êxito.<br/> |



 

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

[**BG_JOB_TIMES**](bg-job-times.md)
</dt> </dl>

 

 





