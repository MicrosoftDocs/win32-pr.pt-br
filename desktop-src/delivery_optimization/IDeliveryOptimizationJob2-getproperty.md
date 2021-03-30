---
title: 'Método IDeliveryOptimizationJob2:: GetProperty'
description: Retorna uma única propriedade do trabalho do.
keywords:
- Método GetProperty
- Método GetProperty, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454885"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>Método IDeliveryOptimizationJob2:: GetProperty

Esse método retorna uma única propriedade do trabalho do.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*propId* \[ no\]
</dt> <dd>

A ID de propriedade necessária a ser obtida. Há suporte apenas para **DOJobPropertyId_ExtendedErrorInfo** do tipo VT_BSTR.

</dd> <dt>

*propvalue* \[ fora\]
</dt> <dd>

O valor da propriedade resultante, armazenado em um tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores de HRESULT a seguir.

| Código de retorno                  | Description          |
|------------------------------|----------------------|
| **S_OK**                     | Sucesso              |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID de propriedade desconhecida. |

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

## <a name="see-also"></a>Consulte também

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
