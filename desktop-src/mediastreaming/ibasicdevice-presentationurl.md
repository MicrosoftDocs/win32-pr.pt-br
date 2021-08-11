---
title: Método IBasicDevice PresentationUrl
description: Recupera a URL de apresentação do dispositivo.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- API de streaming de mídia do método PresentationUrl
- API de streaming de mídia do método PresentationUrl, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método PresentationUrl
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d5908b80e7b413ca646279a751e12ec7d9c7e6e98ae7ecff3ad1f1d9e60bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235933"
---
# <a name="ibasicdevicepresentationurl-method"></a>IBasicDevice: método resentationUrl de:P

Recupera a URL de apresentação do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para a URL de apresentação do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Veja também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





