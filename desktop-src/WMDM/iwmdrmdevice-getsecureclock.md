---
title: Método GetSecureClock IWMDRMDevice
description: O método GetSecureClock recupera o relógio seguro, para que licenças baseadas em tempo possam ser impostas.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Método GetSecureClock windows Media Gerenciador de Dispositivos
- Método GetSecureClock windows Media Gerenciador de Dispositivos , interface IWMDRMDevice
- Interface IWMDRMDevice windows Media Gerenciador de Dispositivos , método GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa9494a594a396550028f083cc2b646f2093f6369ab27ae5494bf70c13628d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619776"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>Método IWMDRMDevice::GetSecureClock

O **método GetSecureClock** recupera o relógio seguro, para que licenças baseadas em tempo possam ser impostas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppbSecureClock* \[ out\]
</dt> <dd>

Relógio seguro recuperado.

</dd> <dt>

*pcbSecureClock* \[ out\]
</dt> <dd>

Tamanho do relógio seguro, em bytes.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Sinalizadores de status do dispositivo. Esse valor deve ser um dos sinalizadores a seguir.



| Sinalizador                     | Descrição                            |
|--------------------------|----------------------------------------|
| \_ \_ ISWMDRM DO DISPOSITIVO WMDRM   | O dispositivo dá suporte Windows DRM de Mídia. |
| \_NEEDCLOCK DO DISPOSITIVO \_ WMDRM | O dispositivo precisa de relógio.                |
| DISPOSITIVO WMDRM \_ \_ REVOGADO   | O dispositivo foi revogado.           |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**IWMDRMDevice Interface**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





