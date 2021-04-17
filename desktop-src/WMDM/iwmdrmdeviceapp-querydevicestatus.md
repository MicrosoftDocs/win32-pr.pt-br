---
title: Método IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: O método QueryDeviceStatus consulta um dispositivo quanto ao seu status e recursos de DRM atuais.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Método QueryDeviceStatus Windows Media Gerenciador de Dispositivos
- Método QueryDeviceStatus Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, método QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759760"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>Método IWMDRMDeviceApp:: QueryDeviceStatus

O método **QueryDeviceStatus** consulta um dispositivo quanto ao seu status e recursos de DRM atuais.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pdwStatus* \[ fora\]
</dt> <dd>

Zero ou mais dos valores **DWORD** a seguir que descrevem os aspectos de DRM do dispositivo, combinados com um **OR bit a** bit. Consulte Observações.



| Status                      | Descrição                                  |
|-----------------------------|----------------------------------------------|
| \_ISWMDRM de dispositivo WMDRM \_      | O dispositivo dá suporte a DRM do Windows Media.       |
| \_NEEDCLOCK de dispositivo WMDRM \_    | O dispositivo não tem um Clock seguro.     |
| \_dispositivo WMDRM \_ revogado      | O dispositivo foi revogado.                 |
| \_NEEDINDIV do cliente WMDRM \_    | A segurança do DRM precisa ser individualizada. |
| \_REFRESHCLOCK de dispositivo WMDRM \_ | O relógio precisa ser atualizado.             |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                              | Descrição                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | O método foi bem-sucedido.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | O argumento de entrada não é válido.<br/>                               |
| <dl> <dt>**certificado inválido do NS \_ E \_ DRM \_ \_**</dt> </dl>          | O certificado de dispositivo recuperado do dispositivo não é válido.<br/> |
| <dl> <dt>**o NS \_ E \_ DRM \_ não pode \_ obter o \_ \_ certificado do dispositivo \_**</dt> </dl> | Falha ao recuperar o certificado do dispositivo do dispositivo.<br/>     |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado antes de executar qualquer ação restrita no conteúdo DRM, como transferir conteúdo DRM para o dispositivo ou adquirir informações de medição. Se os valores recuperados por *pdwStatus* indicarem que alguma ação precisa ser executada (como individualização para a área de trabalho ou aquisição de um relógio para o dispositivo), o aplicativo deverá chamar [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor de *pdwStatus* recuperado dessa função para o parâmetro *dwFlags* em **AcquireDeviceData**. Se zero for retornado, o dispositivo não oferecerá suporte ao Windows Media DRM 10 para dispositivos portáteis e nenhuma ação precisará ser executada. Consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md) para obter mais informações.

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

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





