---
title: Método IWMDRMDevice SetSecureClockResponse
description: O método SetSecureClockResponse define a resposta de relógio segura.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Método SetSecureClockResponse windows Media Gerenciador de Dispositivos
- Método SetSecureClockResponse windows Media Gerenciador de Dispositivos , interface IWMDRMDevice
- Interface IWMDRMDevice windows Media Gerenciador de Dispositivos , método SetSecureClockResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af9dae5e49240ef0095f499cf8abe34d6931caf7c36cf0ec7fc6908c9821a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031856"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>Método IWMDRMDevice::SetSecureClockResponse

O **método SetSecureClockResponse** define a resposta de relógio segura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbResponse* \[ Em\]
</dt> <dd>

A resposta de relógio segura a ser definida.

</dd> <dt>

*cbResponse* \[ Em\]
</dt> <dd>

O tamanho especificado da resposta do relógio seguro, em bytes.

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

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**IWMDRMDevice Interface**](iwmdrmdevice.md)
</dt> </dl>

 

 





