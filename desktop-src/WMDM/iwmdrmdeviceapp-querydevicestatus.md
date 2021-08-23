---
title: Método IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp.h)
description: O método QueryDeviceStatus consulta um dispositivo quanto ao status e às funcionalidades atuais do DRM.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Método QueryDeviceStatus windows Media Gerenciador de Dispositivos
- Método QueryDeviceStatus windows Media Gerenciador de Dispositivos , interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp windows Media Gerenciador de Dispositivos , método QueryDeviceStatus
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
ms.openlocfilehash: b169412104a5e22ae973542457d08bead328ea4ded5a34691499ea8dbfd8b7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055634"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>Método IWMDRMDeviceApp::QueryDeviceStatus

O **método QueryDeviceStatus** consulta um dispositivo quanto ao status e às funcionalidades atuais do DRM.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Ponteiro para um [**objeto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Zero ou mais dos seguintes valores **DWORD** que descrevem os aspectos drm do dispositivo, combinados com um OR bit a **bit.** Consulte Observações.



| Status                      | Descrição                                  |
|-----------------------------|----------------------------------------------|
| \_ \_ ISWMDRM DO DISPOSITIVO WMDRM      | O dispositivo dá suporte Windows DRM de Mídia.       |
| \_NEEDCLOCK DO DISPOSITIVO \_ WMDRM    | O dispositivo não tem um relógio seguro.     |
| DISPOSITIVO WMDRM \_ \_ REVOGADO      | O dispositivo foi revogado.                 |
| \_NEEDINDIV DO \_ CLIENTE WMDRM    | A segurança do DRM precisa ser individualizada. |
| ATUALIZAÇÃO DO \_ DISPOSITIVO WMDRMCLOCK \_ | O relógio precisa ser atualizado.             |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                              | Descrição                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | O método foi bem-sucedido.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | O argumento de entrada não é válido.<br/>                               |
| <dl> <dt>**NS \_ E \_ DRM CERTIFICADO \_ \_ INVÁLIDO**</dt> </dl>          | O certificado do dispositivo recuperado do dispositivo não é válido.<br/> |
| <dl> <dt>**O NS \_ E \_ DRM \_ NÃO CONSEGUE OBTER O CERTIFICADO DO \_ \_ \_ \_ DISPOSITIVO**</dt> </dl> | Falha ao recuperar o certificado do dispositivo.<br/>     |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado antes de executar ações restritas no conteúdo drm, como transferir conteúdo drm para o dispositivo ou adquirir informações de medição. Se os valores recuperados por *pdwStatus* indicarem que alguma ação precisa ser executada (como individualização para a área de trabalho ou aquisição de um relógio para o dispositivo), o aplicativo deverá chamar [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor *pdwStatus* recuperado dessa função para o parâmetro *dwFlags* **em AcquireDeviceData**. Se zero for retornado, o dispositivo não dá suporte Windows DRM de Mídia 10 para Dispositivos Portáteis e nenhuma ação precisa ser tomada. Consulte [Tratamento de conteúdo protegido no aplicativo para](handling-protected-content-in-the-application.md) obter mais informações.

## <a name="examples"></a>Exemplos

O exemplo de código C++ a seguir cria um objeto **WMDRMDeviceApp,** verifica se o dispositivo é um dispositivo drm 10 de mídia do Windows, se seu relógio é preciso e, em seguida, solicita os dados de medição.


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
| parâmetro<br/>  | <dl> <dt>WMDRMDeviceApp.h (também requer Wmdrmdeviceapp \_ i.c, criado do WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Manipulando conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp Interface**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





