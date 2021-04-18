---
title: Método IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: O método GetRootLicenseResponse gera uma mensagem de resposta de licença raiz.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Formato de mídia do Windows do método GetRootLicenseResponse
- Método GetRootLicenseResponse Windows Media Format, interface IWMDRMNetTransmitter
- Formato de mídia do Windows de interface IWMDRMNetTransmitter, método GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767003"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>Método IWMDRMNetTransmitter:: GetRootLicenseResponse

O método **GetRootLicenseResponse** gera uma mensagem de resposta de licença raiz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrKID* \[ no\]
</dt> <dd>

Identificador de chave codificado em base64 a ser usado para a nova licença raiz. O identificador de chave deve ser um valor GUID gerado aleatoriamente.

</dd> <dt>

*ppbLicenseResponse* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o endereço da resposta de licença gerada. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseResponse* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho da resposta de licença, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt> </dl> | Uma lista de revogação de conteúdo atualizada é necessária.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O método foi bem-sucedido.<br/>                         |



 

## <a name="remarks"></a>Comentários

A licença raiz gerada é criada usando as informações dos dados de desafio de licença, que são processados para a interface chamando [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).

A licença raiz é usada na geração de licenças de folha, que é realizada chamando o método [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) . A interface **IWMDRMNetTransmitter** mantém uma cópia da licença raiz para esse uso.

A licença raiz criada chamando esse método não tem nenhuma política e está configurada para que não possa ser persistida no dispositivo receptor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





