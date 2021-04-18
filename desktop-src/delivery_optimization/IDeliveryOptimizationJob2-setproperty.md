---
title: 'Método IDeliveryOptimizationJob2:: SetProperty'
description: Este método não é usado.
keywords:
- Método SetProperty
- Método SetProperty, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369675"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a>Método IDeliveryOptimizationJob2:: SetProperty

Este método não é usado.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*propId* \[ no\]
</dt> <dd>

Não utilizado.

</dd> <dt>

*propvalue* \[ no\]
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se propId for **DOJobPropertyId_ExtendedErrorInfo**, o valor retornado será **DO_E_READ_ONLY_PROPERTY**, caso contrário, a função retornará **DO_E_UNKNOWN_PROPERTY_ID**.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|---------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte  | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]                                   |
| Servidor mínimo com suporte  | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]                               |
| parâmetro                    | Deliveryoptimization. h                                                           |
| INSERI                       | DeliveryOptimization. idl                                                         |
| Biblioteca                   | Dosvc. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Confira também

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
