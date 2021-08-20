---
description: Obtém as propriedades especificadas deste Plug and Play dispositivo.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Método deviceproperties da classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 855c3c0644d8c7b5c5300c8d12d5a6f98073a4511f8d0d65f4058da7fb9d0f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077506"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>Método deviceproperties da \_ classe Win32 PnPEntity

Obtém as propriedades especificadas deste Plug and Play dispositivo.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*devicePropertyKeys* \[ em, opcional\]
</dt> <dd>

As propriedades a serem retornadas.

</dd> <dt>

*dispositivos* \[ fora\]
</dt> <dd>

As propriedades solicitadas nos subtipos apropriados da classe abstrata [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_PnPEntity Win32**](win32-pnpentity.md)
</dt> </dl>

 

 




