---
description: O método GetPropById do objeto DeviceInfo usa a ID de uma propriedade de dispositivo para retornar seu valor.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Método DeviceInfo. GetPropById
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766556"
---
# <a name="deviceinfogetpropbyid-method"></a>Método DeviceInfo. GetPropById

O método **GetPropById** do objeto [**DEVICEINFO**](-wia-deviceinfo.md) usa a ID de uma propriedade de dispositivo para retornar seu valor.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Tipo: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**

Especifica a ID da propriedade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **variante**

Esse método retorna o valor da propriedade especificada por *ID*.

## <a name="remarks"></a>Comentários

Use esse método para localizar o valor de uma propriedade de dispositivo de sua ID. Para obter uma lista de IDs de propriedade, consulte [definições de constante de propriedade WIA](-wia-wia-property-constant-definitions.md). Para obter informações sobre as próprias propriedades de aquisição de imagem do Windows (WIA), consulte [constantes da propriedade WIA](-wia-wia-property-constants.md).

Para aplicativos Microsoft Visual Basic, adicione uma referência a "biblioteca de tipos do Windows Image Acquisition 1, 1". Estas constantes definidas nesse arquivo são válidas para este método:

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso do método **GetPropById** para recuperar um valor de propriedade.


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




