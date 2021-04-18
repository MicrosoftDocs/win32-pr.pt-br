---
title: Método ModelName IBasicDevice
description: Recupera o nome do modelo do dispositivo.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- API de streaming de mídia do método ModelName
- API de streaming de mídia do método ModelName, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ModelName
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105779511"
---
# <a name="ibasicdevicemodelname-method"></a>Método IBasicDevice:: ModelName

Recupera o nome do modelo do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para o nome do modelo do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





