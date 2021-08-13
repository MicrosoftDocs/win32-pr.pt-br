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
ms.openlocfilehash: 35084fafb92b3716208aa6062f065cc4e25a45d2d1a412083076b9e355d2ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735606"
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

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





