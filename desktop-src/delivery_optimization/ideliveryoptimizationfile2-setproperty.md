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
ms.openlocfilehash: 99ed42acb94f260e229abfe9df428aaa61d3658cb887892b84bb73fd6e7e63e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635716"
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

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores de HRESULT a seguir.

| Código de retorno                  | Descrição                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Êxito                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID de propriedade desconhecida                                                |
| **DO_E_INVALID_STATE**       | O trabalho não está atualmente em um estado que permita uma configuração de propriedade |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|---------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte  | Windows 10, \[ somente aplicativos da área de trabalho da versão 1803\]                                   |
| Servidor mínimo com suporte  | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]                               |
| Cabeçalho                    | Deliveryoptimization. h                                                           |
| INSERI                       | DeliveryOptimization. idl                                                         |
| Biblioteca                   | Dosvc. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Confira também

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
