---
title: Método GetState IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera o estado do trabalho.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Método GetState
- Método GetState, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método GetState
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
ms.openlocfilehash: 64a26d1cc301230a9bb8330b9a2b2daf3178b1538ec95f593cd5e3f4d3099d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755296"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>Método IBackgroundCopyJob::GetState

Recupera o estado do trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pJobState* \[ out\]
</dt> <dd>

O estado do trabalho. Por exemplo, o estado reflete se o trabalho está com erro, transferindo dados ou suspenso. Para ver uma lista de estados de trabalho, [**consulte a enumeração BG_JOB_STATE**](bg-job-state-.md) trabalho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                              | Descrição                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | O estado do trabalho foi recuperado com êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Se você quiser saber quando um trabalho está com erro ou tiver transferido todos os arquivos no trabalho, poderá usar esse método para sondar o estado do trabalho ou registrar-se para receber notificação quando ocorrerem eventos. Para obter detalhes sobre como se registrar para receber a notificação de eventos, consulte a interface [**IBackgroundCopyCallback.**](ibackgroundcopycallback.md)

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





