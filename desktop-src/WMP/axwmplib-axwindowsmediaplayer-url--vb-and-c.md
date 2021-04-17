---
title: Propriedade AxWindowsMediaPlayer. URL
description: A propriedade URL Obtém ou define o nome do item de mídia a ser reproduzido.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Propriedade de URL Windows Media Player
- Propriedade de URL Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, propriedade de URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811349"
---
# <a name="axwindowsmediaplayerurl-property"></a>Propriedade AxWindowsMediaPlayer. URL

A propriedade URL Obtém ou define o nome do item de mídia a ser reproduzido.

## <a name="syntax"></a>Syntax


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um System. String que é a URL do item de mídia.

## <a name="remarks"></a>Comentários

Essa propriedade só pode ser definida como uma URL em uma zona de segurança que seja a mesma ou menos restritiva do que a zona de segurança do programa de chamada ou da página da Web.

Os aplicativos que abrirem itens de mídia atrás de um firewall terão um desempenho melhor se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.

Não chame esse método do código do manipulador de eventos. A chamada de **URL** de um manipulador de eventos pode gerar resultados inesperados.

## <a name="examples"></a>Exemplos

O exemplo a seguir permite que o usuário especifique um arquivo de mídia inserindo um caminho de arquivo em uma caixa de texto. Quando um botão é clicado, a propriedade URL é definida como o arquivo especificado e o arquivo é reproduzido. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

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

 

 





