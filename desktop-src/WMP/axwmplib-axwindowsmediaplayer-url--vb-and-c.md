---
title: Propriedade AxWindowsMediaPlayer.URL
description: A propriedade URL obtém ou define o nome do item de mídia a ser reproduzir.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Propriedade url Windows Media Player
- Propriedade url Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player propriedade URL
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
ms.openlocfilehash: d953f2d85fc1fd83edcd37a491cb2f7cbabc3e3dfaf61e48feb1cd30e6d01934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123876"
---
# <a name="axwindowsmediaplayerurl-property"></a>Propriedade AxWindowsMediaPlayer.URL

A propriedade URL obtém ou define o nome do item de mídia a ser reproduzir.

## <a name="syntax"></a>Syntax


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um System.String que é a URL do item de mídia.

## <a name="remarks"></a>Comentários

Essa propriedade só pode ser definida como uma URL em uma zona de segurança que seja a mesma ou seja menos restritiva do que a zona de segurança do programa de chamada ou da página da Web.

Aplicativos que abrem itens de mídia por trás de um firewall terão melhor desempenho se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.

Não chame esse método do código do manipulador de eventos. Chamar **a URL** de um manipulador de eventos pode gerar resultados inesperados.

## <a name="examples"></a>Exemplos

O exemplo a seguir permite que o usuário especifique um arquivo de mídia inserindo um caminho de arquivo em uma caixa de texto. Quando um botão é clicado, a propriedade URL é definida como o arquivo especificado e o arquivo é interpretado. O objeto AxWMPLib.AxWindowsMediaPlayer é representado pela variável chamada player.


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
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





