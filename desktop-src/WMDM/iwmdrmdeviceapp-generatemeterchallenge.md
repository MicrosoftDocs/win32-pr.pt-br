---
title: Método IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp. h)
description: O método GenerateMeterChallenge adquire dados de medição de um dispositivo.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Método GenerateMeterChallenge Windows Media Gerenciador de Dispositivos
- Método GenerateMeterChallenge Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método GenerateMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810596"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>Método IWMDRMDeviceApp:: GenerateMeterChallenge

O método **GenerateMeterChallenge** adquire dados de medição de um dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Ponteiro para uma interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) . Se o aplicativo passar em **NULL**, as informações de medição armazenadas no computador serão usadas em vez de monitorar as informações de um dispositivo conectado.

</dd> <dt>

*bstrMeterCert* \[ no\]
</dt> <dd>

O certificado de medição do aplicativo, como um **BSTR**. Este é um certificado assinado recebido da Microsoft.

</dd> <dt>

*pbstrMeterURL* \[ fora\]
</dt> <dd>

A URL na qual os dados de medição devem ser enviados. Isso é alocado pelo Windows Media Gerenciador de Dispositivos e deve ser gratuito pelo chamador usando **SysFreeString**.

</dd> <dt>

*pbstrMeterData* \[ fora\]
</dt> <dd>

Medição de dados a serem enviados para o serviço de medição. Isso é alocado pelo Windows Media Gerenciador de Dispositivos e deve ser gratuito pelo chamador usando **SysFreeString**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                      | Descrição                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | O método foi bem-sucedido.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Um ou mais argumentos não são válidos.<br/>                               |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>             | O XML está formado incorretamente.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>             | O XML está formado incorretamente.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>              | O XML está formado incorretamente.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>               | Falha ao localizar uma marca XML necessária.<br/>                                 |
| <dl> <dt>**Erros do dispositivo**</dt> </dl>            | Qualquer um dos vários erros do dispositivo.<br/>                                  |
| <dl> <dt>**Erros do cliente DRM**</dt> </dl>        | Qualquer um dos vários erros internos do cliente DRM.<br/>                     |
| <dl> <dt>**dispositivo \_ ns \_ E \_ não \_ WMDRM \_**</dt> </dl> | O dispositivo especificado não é um dispositivo compatível com DRM do Windows Media.<br/> |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, o aplicativo deve chamar [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) para verificar se todos os componentes DRM do dispositivo estão atualizados. Esse método só pode ser chamado em um dispositivo que ofereça suporte ao Windows Media DRM 10 para dispositivos portáteis.

Os dados recuperados *pbstrMeterData* devem ser enviados para a URL especificada por *pbstrMeterURL*. Certifique-se de codificar por URL os dados recuperados para que eles não sejam modificados durante a transferência.

Consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md) para obter mais informações.

## <a name="examples"></a>Exemplos

O exemplo de código C++ a seguir cria um objeto **WMDRMDeviceApp** , verifica se o dispositivo é um dispositivo Windows Media DRM 10, se o relógio está correto e solicita os dados de medição.


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



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

 

 





