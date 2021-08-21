---
title: Propriedade AxWindowsMediaPlayer.versionInfo
description: A propriedade versionInfo obtém um valor que especifica a versão do Windows Media Player.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- Propriedade versionInfo Windows Media Player
- Propriedade versionInfo Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player propriedade , versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd7491af0fc102f03da9855b78ecef79ac0a09ca9b3ab8b49f9bf6b948f0d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841157"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a>Propriedade AxWindowsMediaPlayer.versionInfo

A propriedade versionInfo obtém um valor que especifica a versão do Windows Media Player.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um System.String que são as informações de versão no seguinte formato: "*X*.0.0. *AAAA*" em *que X* representa o número de versão principal e *AAAA representa* o número de build.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um botão que, quando clicado, exibe uma caixa de mensagem contendo as informações de versão para Windows Media Player. O objeto AxWMPLib.AxWindowsMediaPlayer é representado pela variável chamada player.


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





