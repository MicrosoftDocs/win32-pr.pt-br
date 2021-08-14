---
title: Método GetNoProgressTimeout de IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera o período de tempo que o serviço tenta transferir o arquivo depois que ocorre uma condição de erro transitório. Se houver progresso, o temporizador será redefinido.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Método GetNoProgressTimeout
- Método GetNoProgressTimeout, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a80e4d89c510885372a92d2c373d5fb73e9bd8375dd712ec07c5f98be51f791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755426"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a>Método IBackgroundCopyJob::GetNoProgressTimeout

Recupera o período de tempo que o serviço tenta transferir o arquivo depois que ocorre uma condição de erro transitório. Se houver progresso, o temporizador será redefinido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRetryPeriod* \[ Em\]
</dt> <dd>

Período de tempo, em segundos, em que o serviço tenta transferir o arquivo após um erro transitório.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                              | Descrição                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | O tempo-out foi recuperado com êxito.<br/> |



 

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

[**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





