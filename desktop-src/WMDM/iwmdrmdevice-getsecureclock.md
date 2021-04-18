---
title: Método IWMDRMDevice GetSecureClock
description: O método GetSecureClock recupera o relógio seguro, portanto, as licenças baseadas em tempo podem ser impostas.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Método GetSecureClock Windows Media Gerenciador de Dispositivos
- Método GetSecureClock Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método GetSecureClock
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
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810599"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>Método IWMDRMDevice:: GetSecureClock

O método **GetSecureClock** recupera o relógio seguro, portanto, as licenças baseadas em tempo podem ser impostas.

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

*ppbSecureClock* \[ fora\]
</dt> <dd>

Clock seguro recuperado.

</dd> <dt>

*pcbSecureClock* \[ fora\]
</dt> <dd>

Tamanho do relógio seguro, em bytes.

</dd> <dt>

*pdwFlags* \[ fora\]
</dt> <dd>

Sinalizadores de status do dispositivo. Esse valor deve ser um dos sinalizadores a seguir.



| Sinalizador                     | Descrição                            |
|--------------------------|----------------------------------------|
| \_ISWMDRM de dispositivo WMDRM \_   | O dispositivo dá suporte a DRM do Windows Media. |
| \_NEEDCLOCK de dispositivo WMDRM \_ | O dispositivo precisa de relógio.                |
| \_dispositivo WMDRM \_ revogado   | O dispositivo foi revogado.           |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





