---
description: O método Create do objeto DeviceInfo faz uma conexão com o dispositivo de aquisição de imagens do Windows (WIA) especificado pelo objeto DeviceInfo e retorna um objeto item que representa o dispositivo.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: Método DeviceInfo. Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790413"
---
# <a name="deviceinfocreate-method"></a>Método DeviceInfo. Create

O método **Create** do objeto [**DeviceInfo**](-wia-deviceinfo.md) faz uma conexão com o dispositivo de aquisição de imagens do Windows (WIA) especificado pelo objeto **DeviceInfo** e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **IWiaDispatchItem**

Esse método retorna o objeto [**Item**](-wia-item.md) que representa o dispositivo criado.

## <a name="remarks"></a>Comentários

Use o método **Create** para criar uma conexão com um dispositivo de hardware WIA depois de enumerar a coleção de [**dispositivos**](-wia-iwia-devices.md) . O método retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo (um item raiz).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso do método **Create** .


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




