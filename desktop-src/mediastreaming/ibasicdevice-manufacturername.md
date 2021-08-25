---
title: Método ManufacturerName do IBasicDevice
description: Recupera o nome do fabricante do dispositivo.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- API de streaming de mídia do método ManufacturerName
- API de streaming de mídia do método ManufacturerName, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ManufacturerName
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 453e11fc547998b6dc3e39017684c30cacd205c0c17b21846925d4de472f43a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011826"
---
# <a name="ibasicdevicemanufacturername-method"></a>Método IBasicDevice:: ManufacturerName

Recupera o nome do fabricante do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para o nome do fabricante do dispositivo.

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

 

 





