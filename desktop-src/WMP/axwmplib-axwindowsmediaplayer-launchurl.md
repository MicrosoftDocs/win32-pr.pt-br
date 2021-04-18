---
title: Método AxWindowsMediaPlayer. launchURL
description: O método launchURL envia uma URL para o navegador padrão do usuário a ser renderizado. | Método AxWindowsMediaPlayer. launchURL
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- método launchURL Windows Media Player
- método launchURL Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781060"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a>Método AxWindowsMediaPlayer. launchURL

O método launchURL envia uma URL para o navegador padrão do usuário a ser renderizado.

## <a name="syntax"></a>Sintaxe


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrURL* 
</dt> <dd>

O **System. String** que é a URL a ser iniciada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método abre apenas as páginas da Web usando os protocolos HTTP ou HTTPS.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um botão que, quando clicado, exibe o site da Microsoft em uma nova janela do navegador. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





