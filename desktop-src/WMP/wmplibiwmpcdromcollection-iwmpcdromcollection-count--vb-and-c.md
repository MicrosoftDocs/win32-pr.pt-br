---
title: Propriedade Count de IWMPCdromCollection
description: A propriedade Count Obtém o número de unidades de CD e DVD disponíveis no sistema.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- Propriedade Count Windows Media Player
- Propriedade Count Windows Media Player, interface IWMPCdromCollection
- Interface IWMPCdromCollection Windows Media Player, Propriedade Count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766423"
---
# <a name="iwmpcdromcollectioncount-property"></a>Propriedade IWMPCdromCollection:: Count

A propriedade **Count** Obtém o número de unidades de CD e DVD disponíveis no sistema.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é a contagem de unidades disponíveis.

## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

As unidades de DVD são contadas exatamente como unidades de CD. No entanto, o controle ActiveX do Windows Media Player só dá suporte à funcionalidade de DVD para o Windows XP ou posterior. Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa Count para exibir o número de unidades de CD e DVD disponíveis em uma caixa de mensagem. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





