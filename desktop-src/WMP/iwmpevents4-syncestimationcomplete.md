---
title: Método IWMPEvents4 SyncEstimationComplete
description: O evento SyncEstimationComplete ocorre quando uma estimativa de tamanho, iniciada anteriormente pelo IWMPSyncDevice3 estimateSyncSize, é concluída.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Windows Media Player do método SyncEstimationComplete
- método SyncEstimationComplete Windows Media Player, interface IWMPEvents4
- Windows Media Player de interface IWMPEvents4, método SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3f444cdc66874c907bb4c6412fa10384fde67145563d79153c28cb675c6fc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575601"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>Método IWMPEvents4:: SyncEstimationComplete

O evento **SyncEstimationComplete** ocorre quando uma estimativa de tamanho, iniciada anteriormente por [**IWMPSyncDevice3:: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), é concluída.

## <a name="syntax"></a>Sintaxe


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Ponteiro para a interface [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) que representa o dispositivo para o qual a estimativa de tamanho foi iniciada.

</dd> <dt>

*hrResult* \[ no\]
</dt> <dd>

Um valor que indica o êxito ou a falha da estimativa.



| Valor                                                                                                                                       | Significado                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>          | A estimativa foi bem-sucedida.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ anular**</dt> </dl> | A estimativa foi anulada.<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[ no\]
</dt> <dd>

O espaço estimado (em bytes) que seria usado no dispositivo.

</dd> <dt>

*lEstimatedSize* \[ no\]
</dt> <dd>

O tamanho estimado (em bytes) dos dados a serem sincronizados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





