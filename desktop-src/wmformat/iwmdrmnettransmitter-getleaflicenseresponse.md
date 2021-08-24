---
title: Método IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: O método GetLeafLicenseResponse gera uma mensagem de resposta de licença de folha.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Formato de mídia do Windows do método GetLeafLicenseResponse
- Método GetLeafLicenseResponse Windows Media Format, interface IWMDRMNetTransmitter
- Formato de mídia do Windows de interface IWMDRMNetTransmitter, método GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aff470341c3227782d0d34cbdd2ca2a4a51a4cb1b6214b81ea2ea9a384b29ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084826"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>Método IWMDRMNetTransmitter:: GetLeafLicenseResponse

O método **GetLeafLicenseResponse** gera uma mensagem de resposta de licença de folha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrKID* \[ no\]
</dt> <dd>

Identificador de chave codificado em base64 a ser usado para a nova licença de folha. O identificador de chave deve ser um valor GUID gerado aleatoriamente.

</dd> <dt>

*pPolicy* \[ no\]
</dt> <dd>

Ponteiro para a estrutura de [**\_ política WMDRMNET**](wmdrmnet-policy.md) que define a política a ser usada para a licença de folha.

</dd> <dt>

*ppIWMDRMEncrypt* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) que pode ser usada para criptografar dados para a nova licença de folha.

</dd> <dt>

*ppbLicenseResponse* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o endereço da resposta de licença gerada. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseResponse* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho da resposta de licença, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt> </dl> | Uma lista de revogação de conteúdo atualizada é necessária.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O método foi bem-sucedido.<br/>                         |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





