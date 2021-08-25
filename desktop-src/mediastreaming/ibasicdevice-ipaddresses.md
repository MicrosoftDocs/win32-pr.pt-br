---
title: Método IpAddresses IBasicDevice
description: Retorna um vetor de endereços IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- API de streaming de mídia do método IpAddresses
- API de streaming de mídia do método IpAddresses, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc997abb24c007e9e3e4d5c8028762daaca20e434ca4e3ab22fb278f567f998c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847676"
---
# <a name="ibasicdeviceipaddresses-method"></a>Método IBasicDevice:: IpAddresses

Retorna um vetor de endereços IP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe uma coleção enumerável de ponteiros para endereços IP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





