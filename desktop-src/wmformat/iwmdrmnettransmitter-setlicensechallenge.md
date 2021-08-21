---
title: Método IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: o método SetLicenseChallenge processa um desafio de licença enviado por um Windows mídia DRM para o receptor de dispositivos de rede.
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
ms.openlocfilehash: 211f8de60cddb153e157af64ee300a4bbaf327d70a1564fbd9e622008c055cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027564"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>Método IWMDRMNetTransmitter:: SetLicenseChallenge

o método **SetLicenseChallenge** processa um desafio de licença enviado por um Windows mídia DRM para o receptor de dispositivos de rede.

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

## <a name="return-value"></a>Valor retornado

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

 

 





