---
title: Método IBasicDevice ManufacturerUrl
description: Recupera a URL do fabricante do dispositivo.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- API de Streaming de Mídia do método ManufacturerUrl
- Api de Streaming de Mídia do método ManufacturerUrl, interface IBasicDevice
- API de Streaming de Mídia da interface IBasicDevice, método ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 306b4c194d7354b071d4daaf223a17f977b38b44243adaef856f9acffbf49c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972335"
---
# <a name="ibasicdevicemanufacturerurl-method"></a>Método IBasicDevice::ManufacturerUrl

Recupera a URL do fabricante do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe um ponteiro para a URL do fabricante do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





