---
title: Método GetSecureClockChallenge de IWMDRMDevice
description: O método GetSecureClockChallenge recupera o resultado do desafio de relógio seguro.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Método GetSecureClockChallenge windows Media Gerenciador de Dispositivos
- Método GetSecureClockChallenge windows Media Gerenciador de Dispositivos , interface IWMDRMDevice
- Interface IWMDRMDevice windows Media Gerenciador de Dispositivos , método GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaed21ddffb9c2001c3b57d32d34ac9106ede7cecaff723cb95d8cee1c428fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957246"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>Método IWMDRMDevice::GetSecureClockChallenge

O **método GetSecureClockChallenge** recupera o resultado do desafio de relógio seguro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppbChallenge* \[ out\]
</dt> <dd>

Resultado do desafio recuperado.

</dd> <dt>

*pcbChallenge* \[ out\]
</dt> <dd>

Tamanho do resultado do desafio, em bytes.

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

 

 





