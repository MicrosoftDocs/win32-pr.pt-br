---
title: Método IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: O método ProcessRegistrationResponse processa uma resposta de registro enviada pelo transmissor em resposta a um desafio de registro.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Formato de mídia do Windows do método ProcessRegistrationResponse
- Método ProcessRegistrationResponse Windows Media Format, interface IWMDRMNetReceiver
- Formato de mídia do Windows de interface IWMDRMNetReceiver, método ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786945"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a>IWMDRMNetReceiver: método rocessRegistrationResponse de:P

O método **ProcessRegistrationResponse** processa uma resposta de registro enviada pelo transmissor em resposta a um desafio de registro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbRegistrationResponse* \[ no\]
</dt> <dd>

Resposta de registro recebida do transmissor.

</dd> <dt>

*cbRegistrationResponse* \[ no\]
</dt> <dd>

Tamanho da resposta de registro em bytes.

</dd> <dt>

*ppunkCancellationCookie* \[ fora\]
</dt> <dd>

Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona. Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona; Quando o processamento é concluído, o evento MEProximityCompleted é enviado para a interface **IMFMediaEventGenerator** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





