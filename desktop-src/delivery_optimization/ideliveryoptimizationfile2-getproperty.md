---
title: Método IDeliveryOptimizationFile2::GetProperty
description: Esse método retorna uma única propriedade do arquivo DO. | Método IDeliveryOptimizationFile2::GetProperty
keywords:
- Método GetProperty
- Método GetProperty, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f181eebe2aff8ccbbbf6d5400e3d5a78f123e2304567a413ecf4a35357229b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542086"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>Método IDeliveryOptimizationFile2::GetProperty

Esse método retorna uma única propriedade do arquivo DO.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*propId* \[ Em\]
</dt> <dd>

A ID da propriedade necessária para obter do tipo DOFilePropertyId.

</dd> <dt>

*propValue* \[ out\]
</dt> <dd>

O valor da propriedade armazenado em uma VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes valores HRESULT.

| Código de retorno                  | Descrição                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Êxito                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID da propriedade desconhecida.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | A propriedade é Somente gravação e não pode ser lida.      |
| **E_NOT_SET**                | Nenhuma propriedade foi definida por meio do método SetProperty. |
| **E_OUTOFMEMORY**            |  Falha na alocação de memória                          |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|---------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte  | Windows 10, versão 1803 somente \[ aplicativos da área de trabalho\]                                   |
| Servidor mínimo com suporte  | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]                               |
| Cabeçalho                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Biblioteca                   | Dosvc.lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Confira também

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
