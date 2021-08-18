---
title: Método de descrição de IBasicDevice
description: Recupera uma descrição do dispositivo.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- API de streaming de mídia do método de descrição
- API de streaming de mídia do método de descrição, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método de descrição
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cfaf3ba8ca9c74d094aa8cdc15f4c190d6e5141fb11ff255b6e7682b667846d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972345"
---
# <a name="ibasicdevicedescription-method"></a>IBasicDevice: método descrição de:D

Recupera uma descrição do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para a descrição do dispositivo.

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

 

 





