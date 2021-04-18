---
title: Método GetStats IDeliveryOptimizationFile (Deliveryoptimization. h)
description: Retorna o download e o upload de estatísticas para um arquivo específico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- Método GetStats
- Método GetStats, interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, método GetStats
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369831"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>Método IDeliveryOptimizationFile:: GetStats

Retorna o download e o upload de estatísticas para um arquivo específico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*swarmStats* \[ fora\]
</dt> <dd>

Retorna o download e o upload de estatísticas para um arquivo específico. Consulte a estrutura [**DOSwarmStats**](doswarmstats.md) para obter detalhes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método deve retornar **S_OK**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile é definido como B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





