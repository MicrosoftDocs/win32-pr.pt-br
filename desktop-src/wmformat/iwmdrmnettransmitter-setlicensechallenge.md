---
title: Método IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: O método SetLicenseChallenge processa um desafio de licença enviado por um receptor do Windows Media DRM para dispositivos de rede.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Formato de mídia do Windows do método SetLicenseChallenge
- Método SetLicenseChallenge Windows Media Format, interface IWMDRMNetTransmitter
- Formato de mídia do Windows de interface IWMDRMNetTransmitter, método SetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789913"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>Método IWMDRMNetTransmitter:: SetLicenseChallenge

O método **SetLicenseChallenge** processa um desafio de licença enviado por um receptor do Windows Media DRM para dispositivos de rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbLicenseChallenge* \[ no\]
</dt> <dd>

Ponteiro para os dados de desafio de licença que foram enviados por um receptor.

</dd> <dt>

*cbLicenseChallenge* \[ no\]
</dt> <dd>

Tamanho do desafio de licença em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se esse método tiver sucesso, as chamadas subsequentes para os outros métodos de **IWMDRMNetTransmitter** usarão as informações no desafio processado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





