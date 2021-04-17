---
title: Método IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: O método GetLicenseChallenge gera um desafio de licença do Windows Media DRM para dispositivos de rede que pode ser enviado para um transmissor ao solicitar conteúdo protegido.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Formato de mídia do Windows do método GetLicenseChallenge
- Método GetLicenseChallenge Windows Media Format, interface IWMDRMNetReceiver
- Formato de mídia do Windows de interface IWMDRMNetReceiver, método GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766284"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a>Método IWMDRMNetReceiver:: GetLicenseChallenge

O método **GetLicenseChallenge** gera um desafio de licença do Windows Media DRM para dispositivos de rede que pode ser enviado para um transmissor ao solicitar conteúdo protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAction* \[ no\]
</dt> <dd>

Ação para a qual gerar o desafio.

</dd> <dt>

*ppbLicenseChallenge* \[ fora\]
</dt> <dd>

Endereço de um ponteiro que é definido como o endereço do desafio gerado. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseChallenge* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho do desafio de licença em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

[**IWMDRMNetReceiver::P rocessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





