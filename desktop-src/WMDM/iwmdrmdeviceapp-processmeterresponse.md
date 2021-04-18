---
title: Método IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: O método ProcessMeterResponse redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo tiverem sido enviados e processados pelo servidor.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Método ProcessMeterResponse Windows Media Gerenciador de Dispositivos
- Método ProcessMeterResponse Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método ProcessMeterResponse
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
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800184"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>IWMDRMDeviceApp: método rocessMeterResponse de:P

O método **ProcessMeterResponse** redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo tiverem sido enviados e processados pelo servidor.

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

*pDevice* \[ no\]
</dt> <dd>

Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pbResponse* \[ no\]
</dt> <dd>

Resposta recebida de um servidor de medição depois de enviar dados gerados usando [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).

</dd> <dt>

*cbResponse* \[ no\]
</dt> <dd>

Tamanho de *pbResponse*, em bytes.

</dd> <dt>

*pdwFlags* \[ fora\]
</dt> <dd>

Um **DWORD** da tabela a seguir que indica se há mais dados de medição no dispositivo que precisam ser processados.



| Sinalizador                            | Descrição                                     |
|---------------------------------|-------------------------------------------------|
| \_ \_ todas as respostas de medidor de WMDRM \_     | Todos os dados de medição foram processados.           |
| \_parcial de \_ resposta de medidor de WMDRM \_ | Dados de medição adicionais precisam ser processados. |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                      | Descrição                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | O método foi bem-sucedido.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Um ou mais argumentos não são válidos.<br/>                               |
| <dl> <dt>**Erros do dispositivo**</dt> </dl>            | Qualquer um dos vários erros do dispositivo.<br/>                                  |
| <dl> <dt>**Erros do cliente DRM**</dt> </dl>        | Qualquer um dos vários erros internos do cliente DRM.<br/>                     |
| <dl> <dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt> </dl> | O dispositivo especificado não é um dispositivo compatível com DRM do Windows Media.<br/> |



 

## <a name="remarks"></a>Comentários

Mais informações sobre medição, incluindo exemplos de código, podem ser encontradas no White Paper [monitorando o uso de conteúdo de mídia digital com o Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) no site do MSDN.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lidando com conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interface IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

