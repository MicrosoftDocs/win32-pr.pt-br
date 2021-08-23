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
ms.openlocfilehash: f4e2f0a3b680e682944740cb570bfb4889b22ba8e7ec56d3aefc9e34fcdd6a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635756"
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

## <a name="return-value"></a>Valor retornado

Esse método deve retornar **S_OK**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile é definido como B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





