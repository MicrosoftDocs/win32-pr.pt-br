---
title: Método IBasicDevice ModelNumber
description: Recupera o número do modelo do dispositivo.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- API de streaming de mídia do método ModelNumber
- API de streaming de mídia do método ModelNumber, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823227"
---
# <a name="ibasicdevicemodelnumber-method"></a>Método IBasicDevice:: ModelNumber

Recupera o número do modelo do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para o número do modelo do dispositivo.

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

 

 





