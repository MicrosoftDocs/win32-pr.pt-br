---
title: Método IBasicDevice DiscoveredOnCurrentNetwork
description: Recupera um valor que indica se o dispositivo está na rede atual.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- API de Streaming de Mídia do método DiscoveredOnCurrentNetwork
- API de Streaming de Mídia do método DiscoveredOnCurrentNetwork, interface IBasicDevice
- API de Streaming de Mídia da interface IBasicDevice , método DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 605962315e4eab2cdbd5beab264747d282d78ef7c6f44b3bbcbf2f249bac7548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473485"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>Método IBasicDevice::D iscoveredOnCurrentNetwork

Recupera um valor que indica se o dispositivo está na rede atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe um ponteiro para um valor booliana que é **True** se o dispositivo estiver na rede atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





