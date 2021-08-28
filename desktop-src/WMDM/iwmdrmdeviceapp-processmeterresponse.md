---
title: Método IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp.h)
description: O método ProcessMeterResponse redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo são enviados e processados pelo servidor.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Método ProcessMeterResponse windows Media Gerenciador de Dispositivos
- Método ProcessMeterResponse windows Media Gerenciador de Dispositivos , interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp windows Media Gerenciador de Dispositivos , método ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e20338482533293559f135a221b90220f1e371137b3bc1d62502cb3f2e779b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766446"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>Método IWMDRMDeviceApp::P rocessMeterResponse

O **método ProcessMeterResponse** redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo são enviados e processados pelo servidor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Ponteiro para um [**objeto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pbResponse* \[ Em\]
</dt> <dd>

Resposta recebida de um servidor de medição, depois de enviar dados gerados [**usando GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).

</dd> <dt>

*cbResponse* \[ Em\]
</dt> <dd>

Tamanho de *pbResponse*, em bytes.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Um **DWORD** da tabela a seguir que indica se há mais dados de medição no dispositivo que precisam ser processados.



| Sinalizador                            | Descrição                                     |
|---------------------------------|-------------------------------------------------|
| RESPOSTA DO MEDIDOR WMDRM \_ \_ \_ ALL     | Todos os dados de medição foram processados.           |
| RESPOSTA DO MEDIDOR WMDRM \_ \_ \_ PARCIAL | Dados de medição adicionais precisam ser processados. |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                      | Descrição                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | O método foi bem-sucedido.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Um ou mais argumentos não são válidos.<br/>                               |
| <dl> <dt>**Erros do dispositivo**</dt> </dl>            | Qualquer um de vários erros de dispositivo.<br/>                                  |
| <dl> <dt>**Erros do cliente DRM**</dt> </dl>        | Qualquer um de vários erros internos do cliente DRM.<br/>                     |
| <dl> <dt>**NS \_ E \_ DEVICE \_ NOT \_ WMDRM \_ DEVICE**</dt> </dl> | O dispositivo especificado não é um dispositivo compatível Windows DRM de mídia.<br/> |



 

## <a name="remarks"></a>Comentários

Mais informações sobre medição, incluindo exemplos de código, podem ser encontradas no whitepaper Medição do uso de conteúdo de mídia digital com Windows DRM de mídia [10](/previous-versions//bb614723(v=vs.85)) no site do MSDN.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDRMDeviceApp.h (também requer Wmdrmdeviceapp \_ i.c, criado do WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Manipulando conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMDevice Interface**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**IWMDRMDeviceApp Interface**](iwmdrmdeviceapp.md)
</dt> </dl>

 

