---
title: 'Método IDeliveryOptimizationFile2:: GetProperty'
description: 'Esse método retorna uma única propriedade do arquivo do. | Método IDeliveryOptimizationFile2:: GetProperty'
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
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298394"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>Método IDeliveryOptimizationFile2:: GetProperty

Esse método retorna uma única propriedade do arquivo do.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*propId* \[ no\]
</dt> <dd>

A ID de propriedade necessária para obter do tipo DOFilePropertyId.

</dd> <dt>

*propvalue* \[ fora\]
</dt> <dd>

O valor da propriedade armazenado em uma variante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores de HRESULT a seguir.

| Código de retorno                  | Descrição                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Êxito                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID de propriedade desconhecida.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | A propriedade é somente gravação e não pode ser lida.      |
| **E_NOT_SET**                | Nenhuma propriedade foi definida por meio do método SetProperty. |
| **E_OUTOFMEMORY**            |  Falha de alocação de memória                          |

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
