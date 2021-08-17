---
title: Método ProcessLicenseResponse IWMDRMNetReceiver (Wmdrmsdk.h)
description: O método ProcessLicenseResponse processa a resposta de licença enviada pelo transmissor em resposta a um desafio de licença.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Formato de mídia do windows do método ProcessLicenseResponse
- Formato de mídia do método ProcessLicenseResponse , interface IWMDRMNetReceiver
- IWMDRMNetReceiver interface windows Media Format , método ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7ba84c7bf58091bb17500b0d35390062710a79a9a32b939ac8b9517cbcfaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700820"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>Método IWMDRMNetReceiver::P rocessLicenseResponse

O **método ProcessLicenseResponse** processa a resposta de licença enviada pelo transmissor em resposta a um desafio de licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbLicenseResponse* \[ Em\]
</dt> <dd>

Resposta de licença recebida do transmissor.

</dd> <dt>

*cbLicenseResponse* \[ Em\]
</dt> <dd>

Tamanho da resposta em bytes.

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe o endereço da representação de licença interna para a licença contida na mensagem de resposta da licença. Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree.** Esse parâmetro pode ser definido como **NULL se** a representação de licença não for necessária.

</dd> <dt>

*pcbWMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe o tamanho da representação de licença. Deve ser definido como **NULL** se *ppbWMDRMNetLicenseRepresentation* for **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV MUITO \_ \_ PEQUENO**</dt> </dl> | Uma lista de revogação de conteúdo atualizada é necessária.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O método foi bem-sucedido.<br/>                         |



 

## <a name="remarks"></a>Comentários

A resposta de licença processada usando esse método deve corresponder ao último desafio de licença gerado no computador cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMNetReceiver Interface**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





