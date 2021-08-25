---
title: Método IWMDRMDevice IsWMDRMDevice
description: o método IsWMDRMDevice determina se o dispositivo dá suporte a Windows mídia DRM 10 para dispositivos portáteis.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Método IsWMDRMDevice Windows Media Gerenciador de Dispositivos
- Método IsWMDRMDevice Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ee225267ce2301e9a2dad392d72ce72b0e698872cd3fd54ab3e50a07043477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957256"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>Método IWMDRMDevice:: IsWMDRMDevice

o método **IsWMDRMDevice** determina se o dispositivo dá suporte a Windows mídia DRM 10 para dispositivos portáteis.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwVersion* \[ fora\]
</dt> <dd>

versão do Windows Media DRM 10 para dispositivos portáteis, que tem o valor de 0x00010000.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





