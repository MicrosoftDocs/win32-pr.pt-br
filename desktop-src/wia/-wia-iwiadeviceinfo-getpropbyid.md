---
description: O método GetPropById do objeto DeviceInfo usa a ID de uma propriedade de dispositivo para retornar seu valor.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Método DeviceInfo.GetPropById
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
ms.openlocfilehash: c996989661703c4a9c7416cd63904c376fdb7fcca3071d4558551bdd78470d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208782"
---
# <a name="deviceinfogetpropbyid-method"></a>Método DeviceInfo.GetPropById

O **método GetPropById** do [**objeto DeviceInfo**](-wia-deviceinfo.md) usa a ID de uma propriedade de dispositivo para retornar seu valor.

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

## <a name="return-value"></a>Valor retornado

Tipo: **VARIANT**

Esse método retorna o valor da propriedade especificada pela *ID*.

## <a name="remarks"></a>Comentários

Use esse método para encontrar o valor de uma propriedade de dispositivo de sua ID. Para ver uma lista de IDs de propriedade, consulte [Definições de constante](-wia-wia-property-constant-definitions.md)de propriedade WIA . Para obter informações sobre Windows wia (aquisição de imagem) em si, consulte [Constantes de propriedade WIA](-wia-wia-property-constants.md).

Para aplicativos Visual Basic Microsoft, adicione uma referência à "biblioteca de tipos Windows image acquisition 1.01". As seguintes constantes definidas nesse arquivo são válidas para este método:

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

O exemplo a seguir demonstra o uso do **método GetPropById** para recuperar um valor da propriedade.


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




