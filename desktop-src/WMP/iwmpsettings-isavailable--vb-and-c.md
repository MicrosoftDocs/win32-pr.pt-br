---
title: IWMPSettings. IsAvailable (VB e C)
description: A propriedade IsAvailable (o \_ método Get IsAvailable em C \) Obtém um valor que indica se uma ação especificada pode ser executada.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. IsAvailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590979677e79073466f7511b3f382a4bfcebc8bf0fd8ad4cb10f6dcd957db28a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135369"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>IWMPSettings. IsAvailable (VB e C#)

A propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) Obtém um valor que indica se uma ação especificada pode ser executada.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Parâmetros

*bstrItem*

Um **System. String** que é um dos valores a seguir.



| Valor              | Descrição                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| AutoStart          | descobre se a propriedade autostart pode ser definida para especificar que Windows Media Player iniciará a reprodução automaticamente. |
| Saldo            | Descobre se a propriedade de saldo pode ser usada para definir o saldo de estéreo.                                           |
| BaseURL            | Descobre se a propriedade baseURL pode ser definida para especificar uma URL base.                                                |
| DefaultFrame       | Descobre se a propriedade DefaultFrame pode ser definida para especificar o quadro padrão.                                    |
| EnableErrorDialogs | Descobre se a propriedade enableErrorDialogs pode ser definida para habilitar ou desabilitar a exibição de caixas de diálogo de erro.        |
| GetMode            | Descobre se o método GetMode pode ser usado para recuperar o modo de loop atual ou de ordem aleatória.                          |
| InvokeURLs         | Descobre se a propriedade invokeURLs pode ser definida para especificar se os eventos de URL devem iniciar um navegador da Web.         |
| Mute               | Descobre se a propriedade MUTE pode ser definida para especificar se a saída de áudio está ativada ou desativada.                        |
| PlayCount          | Descobre se a propriedade playCount pode ser definida para especificar o número de vezes que um item de mídia será reproduzido.                 |
| Tarifa               | Descobre se a propriedade de taxa pode ser definida para controlar a taxa de reprodução.                                            |
| Setmode            | Descobre se o método setmode pode ser usado para especificar o modo de loop ou de ordem aleatória atual.                           |
| Volume             | Descobre se a propriedade do volume pode ser definida para especificar o volume de áudio.                                           |



 

## <a name="property-value"></a>Valor da propriedade

Um valor **System. booliano** que indica se a ação especificada pode ser executada.

## <a name="remarks"></a>Comentários

**IWMPSettings. isidêntico** é uma propriedade em Visual Basic que usa um parâmetro. Em C#, ele é chamado de método **IWMPSettings. get \_ isidêntico** .

## <a name="examples"></a>Exemplos

O exemplo a seguir testa cada uma das propriedades **IWMPSettings** usando a propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#). O nome da propriedade e o resultado de cada teste são exibidos em uma caixa de texto de várias linhas. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. AutoStart (VB e C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Balance (VB e C#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB e C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. DefaultFrame (VB e C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. GetMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. mudo (VB e C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. playCount (VB e C#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. Rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. volume (VB e C#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





