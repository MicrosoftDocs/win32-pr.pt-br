---
title: Método UniqueDeviceName de IBasicDevice
description: Recupera o UDN (nome exclusivo do dispositivo).
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- API de Streaming de Mídia do método UniqueDeviceName
- API de Streaming de Mídia do método UniqueDeviceName, interface IBasicDevice
- API de Streaming de Mídia da interface IBasicDevice, método UniqueDeviceName
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b70fbc2021cf717cdb49d8a222aa33ad4e9213f297364b81af065c3bbeaed99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972315"
---
# <a name="ibasicdeviceuniquedevicename-method"></a>Método IBasicDevice::UniqueDeviceName

Recupera o UDN (nome exclusivo do dispositivo).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe um ponteiro para o UDN do modelo do dispositivo.

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

 

 





