---
title: Método IWMDRMDevice GetMeterChallenge
description: O método GetMeterChallenge recupera o desafio de medição.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Método GetMeterChallenge Windows Media Gerenciador de Dispositivos
- Método GetMeterChallenge Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781294"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>Método IWMDRMDevice:: GetMeterChallenge

O método **GetMeterChallenge** recupera o desafio de medição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrMeterCert* \[ no\]
</dt> <dd>

Certificado de medição que o proprietário do conteúdo envia ao computador host para coletar os dados de medição associados no dispositivo

</dd> <dt>

*ppbMeterChallenge* \[ fora\]
</dt> <dd>

Resultado do desafio de medição recuperado.

</dd> <dt>

*pcbMeterChallenge* \[ fora\]
</dt> <dd>

O tamanho do desafio de medição, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

A medição de dados é coletada e armazenada no armazenamento de dados DRM no dispositivo para conteúdo com medição habilitada. Ações como reproduzir serão registradas. Quando essa função é chamada, o dispositivo coleta os dados de medição no armazenamento de dados DRM na forma de um documento XML e os envia para o hostcomputer. Se houver muitos dados, eles serão enviados em fases.

Quando o computador host recebe os dados de medição, ele envia os dados pela Internet para a URL especificada no certificado de medição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





