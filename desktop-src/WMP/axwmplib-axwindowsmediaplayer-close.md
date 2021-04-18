---
title: Método AxWindowsMediaPlayer. Close
description: O método Close fecha o arquivo de mídia digital atual, interrompe a reprodução no Windows Media Player e libera os recursos do Windows Media Player.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- fechar o método Windows Media Player
- método Close Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, método Close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800168"
---
# <a name="axwindowsmediaplayerclose-method"></a>Método AxWindowsMediaPlayer. Close

O método Close fecha o arquivo de mídia digital atual, interrompe a reprodução no Windows Media Player e libera os recursos do Windows Media Player.

## <a name="syntax"></a>Sintaxe


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método fecha o arquivo de mídia digital atual, não o Windows Media Player em si.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um botão que, quando clicado, interrompe a reprodução no Windows Media Player e libera os recursos em uso. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

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

 

 





