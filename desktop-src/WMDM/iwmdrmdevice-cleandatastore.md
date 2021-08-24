---
title: Método IWMDRMDevice CleanDataStore
description: O método CleanDataStore inicia o processo de limpeza do armazenamento de dados DRM no dispositivo.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Método CleanDataStore windows Media Gerenciador de Dispositivos
- Método CleanDataStore windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice windows Media Gerenciador de Dispositivos , método CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9decc999d1ecb6c97359d1c4c169b84e7f67da88f5fa25bfe2cb17b2c31f9fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766636"
---
# <a name="iwmdrmdevicecleandatastore-method"></a>Método IWMDRMDevice::CleanDataStore

O **método CleanDataStore** inicia o processo de limpeza do armazenamento de dados DRM no dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Sinalizadores para critérios de limpeza do armazenamento.

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

[**IWMDRMDevice Interface**](iwmdrmdevice.md)
</dt> </dl>

 

 





