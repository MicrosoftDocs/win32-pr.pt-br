---
title: Método IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: O método QueryDeviceStatus2 consulta um dispositivo em busca de um status ou recurso DRM específico.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Método QueryDeviceStatus2 Windows Media Gerenciador de Dispositivos
- Método QueryDeviceStatus2 Windows Media Gerenciador de Dispositivos, interface IWMDRMDeviceApp2
- Interface IWMDRMDeviceApp2 Windows Media Gerenciador de Dispositivos, método QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781471"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a>Método IWMDRMDeviceApp2:: QueryDeviceStatus2

O método **QueryDeviceStatus2** consulta um dispositivo em busca de um status ou recurso DRM específico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Ponteiro para um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um ou mais dos valores **DWORD** a seguir que especificam quais recursos a serem solicitados, combinados com um **OR bit a** bit.



| Sinalizador                              | Descrição                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| \_INDIVSTATUS do \_ cliente de consulta WMDRM \_ | Consulte se os componentes DRM do computador precisam ser individualizados.       |
| \_CLOCKSTATUS de \_ dispositivo de consulta WMDRM \_ | Consulte se o relógio seguro do dispositivo precisa ser adicionado ou atualizado.        |
| \_dispositivo de consulta WMDRM \_ \_ isrevoged   | Consulte se o dispositivo foi revogado.                                         |
| \_ISWMDRM de \_ dispositivo de consulta WMDRM \_     | Consulte se o dispositivo dá suporte a Windows Media DRM 10 para dispositivos portáteis. |



 

</dd> <dt>

*pdwStatus* \[ fora\]
</dt> <dd>

Zero ou mais dos valores **DWORD** a seguir que especificam o status do dispositivo solicitado, combinado com um **OR bit a** bit.



| Status                      | Descrição                                              |
|-----------------------------|----------------------------------------------------------|
| \_ISWMDRM de dispositivo WMDRM \_      | O dispositivo dá suporte a DRM do Windows Media.                   |
| \_NEEDCLOCK de dispositivo WMDRM \_    | O dispositivo não tem um Clock seguro.                 |
| \_dispositivo WMDRM \_ revogado      | O dispositivo foi revogado.                             |
| \_NEEDINDIV do cliente WMDRM \_    | Os componentes DRM do computador precisam ser individualizados. |
| \_REFRESHCLOCK de dispositivo WMDRM \_ | O relógio precisa ser atualizado.                         |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                              | Descrição                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | O método foi bem-sucedido.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | Um ou mais argumentos não são válidos.<br/>                           |
| <dl> <dt>**certificado inválido do NS \_ E \_ DRM \_ \_**</dt> </dl>          | O certificado de dispositivo recuperado do dispositivo não é válido.<br/> |
| <dl> <dt>**o NS \_ E \_ DRM \_ não pode \_ obter o \_ \_ certificado do dispositivo \_**</dt> </dl> | Falha ao recuperar o certificado do dispositivo do dispositivo.<br/>     |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado antes de executar qualquer ação restrita no conteúdo DRM, como transferir conteúdo DRM para o dispositivo ou adquirir informações de medição. Se os valores recuperados por *pdwStatus* indicarem que alguma ação precisa ser executada (como individualização para a área de trabalho ou aquisição de um relógio para o dispositivo), o aplicativo deverá chamar [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor *pdwStatus* recuperado dessa função para o parâmetro *dwFlags* em **AcquireDeviceData**. Se zero for retornado, o dispositivo não oferecerá suporte ao Windows Media DRM 10 para dispositivos portáteis e nenhuma ação precisará ser executada. Consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md) para obter mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDRMDeviceApp. h (também requer Wmdrmdeviceapp \_ i. c, criado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lidando com conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[**Interface IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





