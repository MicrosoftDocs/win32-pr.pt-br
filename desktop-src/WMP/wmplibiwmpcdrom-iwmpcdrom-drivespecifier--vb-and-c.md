---
title: Propriedade IWMPCdrom driveSpecifier
description: A propriedade driveSpecifier Obtém a letra da unidade de CD ou DVD.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- Propriedade driveSpecifier Windows Media Player
- Propriedade driveSpecifier Windows Media Player, interface IWMPCdrom
- Interface IWMPCdrom Windows Media Player, Propriedade driveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811591"
---
# <a name="iwmpcdromdrivespecifier-property"></a>IWMPCdrom: Propriedade riveSpecifier de:d

A propriedade **driveSpecifier** Obtém a letra da unidade de CD ou DVD.

## <a name="syntax"></a>Syntax


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é a letra da unidade.

## <a name="remarks"></a>Comentários

Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD.

Essa propriedade Obtém uma letra da unidade para um índice de unidade com base em zero dentro do intervalo recuperado usando **IWMPCdromCollection. Count**. O valor recuperado assume a forma *X*:, em que *X* representa a letra da unidade.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **driveSpecifier** para criar uma cadeia de caracteres que contém uma lista de unidades de CD e DVD disponíveis e exibe essa cadeia de caracteres em uma caixa de mensagem. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdromCollection. Count (VB e C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





