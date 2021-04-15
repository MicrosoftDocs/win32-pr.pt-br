---
description: O método Create do objeto WIA faz uma conexão com o dispositivo de aquisição de imagem do Windows (WIA) especificado e retorna um objeto item que representa o dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Método WIA. Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505893"
---
# <a name="wiacreate-method"></a>Método WIA. Create

O método **Create** do objeto [**WIA**](-wia-wia.md) faz uma conexão com o dispositivo de aquisição de imagem do Windows (WIA) especificado e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dispositivo* \[ do no\]
</dt> <dd>

Tipo: **Variant \** _

Especifica o dispositivo WIA ao qual se conectar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *IWiaDispatchItem**

Se for bem-sucedido, esse método retornará um objeto [**Item**](-wia-item.md) que representa um dispositivo de hardware WIA (um item raiz).

## <a name="remarks"></a>Comentários

O parâmetro de *dispositivo* especifica um objeto [**DeviceInfo**](-wia-deviceinfo.md) passando o próprio objeto, seu índice de um objeto de coleção ou o valor de sua propriedade de [**ID**](-wia-iwiadeviceinfo-id.md) . Não passe **nada** para exibir uma caixa de diálogo que permita que um usuário selecione um dispositivo.

## <a name="examples"></a>Exemplos

Os exemplos de VBScript a seguir demonstram o uso do método **Create** .

O primeiro exemplo passa um objeto [**DeviceInfo**](-wia-deviceinfo.md) para o método **Create** . Observe que a passagem da propriedade [**ID**](-wia-iwiadeviceinfo-id.md) do objeto causa exatamente o mesmo comportamento.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



No próximo exemplo, o aplicativo de chamada passa o índice do objeto [**DeviceInfo**](-wia-deviceinfo.md) na coleção para o método **Create** .


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



O exemplo a seguir não transmite **nada** para o método **Create** para exibir uma caixa de diálogo que permite que um usuário selecione um dispositivo.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




