---
title: Método IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: o método GetRegistrationChallenge gera uma mensagem de desafio de registro Windows Media DRM para dispositivos de rede.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Formato de mídia do Windows do método GetRegistrationChallenge
- Método GetRegistrationChallenge Windows Media Format, interface IWMDRMNetReceiver
- Formato de mídia do Windows de interface IWMDRMNetReceiver, método GetRegistrationChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6c066de9c455006bfa7e500a30ac290299956ba03a6b4d8df6652a60a75a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701031"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>Método IWMDRMNetReceiver:: GetRegistrationChallenge

o método **GetRegistrationChallenge** gera uma mensagem de desafio de registro Windows Media DRM para dispositivos de rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppbRegistrationChallenge* \[ fora\]
</dt> <dd>

Endereço de um ponteiro que recebe o endereço do desafio gerado. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.

</dd> <dt>

*pcbRegistrationChallenge* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho do desafio de registro em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





