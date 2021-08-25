---
title: Método IBasicDevice ModelUrl
description: Recupera a URL do modelo do dispositivo.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API de streaming de mídia do método ModelUrl
- API de streaming de mídia do método ModelUrl, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7595af295b0d0bc565d79bf5450ee6c5c16b0da4f3baa4fcf636e4e5386920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847646"
---
# <a name="ibasicdevicemodelurl-method"></a>Método IBasicDevice:: ModelUrl

Recupera a URL do modelo do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para a URL do modelo do dispositivo.

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

 

 





