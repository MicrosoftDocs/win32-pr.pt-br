---
title: Método FriendlyName IBasicDevice
description: Recupera o nome amigável do dispositivo.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- API de streaming de mídia do método FriendlyName
- API de streaming de mídia do método FriendlyName, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método FriendlyName
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638590"
---
# <a name="ibasicdevicefriendlyname-method"></a>Método IBasicDevice:: FriendlyName

Recupera o nome amigável do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para o nome amigável do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





