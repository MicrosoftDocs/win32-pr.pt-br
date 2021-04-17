---
title: 'Método IDeliveryOptimizationFile2:: SetProperty'
description: 'Esse método retorna uma única propriedade do arquivo do. | Método IDeliveryOptimizationFile2:: SetProperty'
keywords:
- Método SetProperty
- Método SetProperty, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105811969"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>Método IDeliveryOptimizationFile2:: SetProperty

Esse método retorna uma única propriedade do arquivo do.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*propId* \[ no\]
</dt> <dd>

A ID de propriedade necessária para definir o tipo DOFilePropertyId.

</dd> <dt>

*propvalue* \[ no\]
</dt> <dd>

O valor da propriedade a ser definido, do tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores de HRESULT a seguir.

| Código de retorno                  | Description                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Sucesso                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID de propriedade desconhecida                                                |
| **DO_E_INVALID_STATE**       | O trabalho não está atualmente em um estado que permita uma configuração de propriedade |

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

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
