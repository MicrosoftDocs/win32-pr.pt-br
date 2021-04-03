---
title: Método de método ibackgroundcopyjob prepriorion (Deliveryoptimization. h)
description: Especifica o nível de prioridade do seu trabalho. O nível de prioridade determina quando seu trabalho é processado em relação a outros trabalhos na fila de transferência.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Método setanteriority
- Método setanteriority, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método setanteriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644703"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>Método método ibackgroundcopyjob:: prepriorion

Especifica o nível de prioridade do seu trabalho. O nível de prioridade determina quando seu trabalho é processado em relação a outros trabalhos na fila de transferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Prioridade* \[ do no\]
</dt> <dd>

Especifica o nível de prioridade do seu trabalho em relação a outros trabalhos na fila de transferência. O padrão é BG_JOB_PRIORITY_NORMAL. Para obter uma lista de níveis de prioridade, consulte a enumeração [**BG_JOB_PRIORITY**](bg-job-priority-.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | A prioridade do trabalho foi definida com êxito.<br/> |



 

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

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: getanteriority**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





