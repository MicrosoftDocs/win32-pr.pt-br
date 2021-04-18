---
title: Método Getmétodo ibackgroundcopyjobname (Deliveryoptimization. h)
description: Recupera o nível de prioridade para o trabalho. O nível de prioridade determina quando o trabalho é processado em relação a outros trabalhos na fila de transferência.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- Método getanteriority
- Método getanteriority, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método getanteriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784976"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a>Método método ibackgroundcopyjob:: getanteriority

Recupera o nível de prioridade para o trabalho. O nível de prioridade determina quando o trabalho é processado em relação a outros trabalhos na fila de transferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPriority* \[ fora\]
</dt> <dd>

Prioridade do trabalho em relação a outros trabalhos na fila de transferência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | O nível de prioridade foi recuperado com êxito.<br/> |



 

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

[**Método ibackgroundcopyjob:: setanteriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





