---
description: Coleção de objetos DeviceInfo que representa todos os dispositivos instalados no computador.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Propriedade Wia.Devices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b6cf843d92b5ce2260578b653a1163526b22fb735c01542d772b2687ca890dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208919"
---
# <a name="wiadevices-property"></a>Propriedade Wia.Devices

Coleção de [**objetos DeviceInfo**](-wia-deviceinfo.md) que representa todos os dispositivos instalados no computador. Somente leitura.

> [!Note]  
> Essa coleção é baseada em 0.

 

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

O exemplo a seguir ilustra o uso da coleção **Dispositivos** para enumerar os dispositivos em um sistema.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




