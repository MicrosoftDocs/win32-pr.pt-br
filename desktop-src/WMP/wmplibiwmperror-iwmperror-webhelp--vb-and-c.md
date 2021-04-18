---
title: Método WebHelp do IWMPError
description: O método WebHelp inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero). | Método WebHelp do IWMPError
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- método WebHelp do Windows Media Player
- método WebHelp do Windows Media Player, interface IWMPError
- Interface IWMPError Windows Media Player, método Webhelp
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764524"
---
# <a name="iwmperrorwebhelp-method"></a>Método IWMPError:: Webhelp

O método **WebHelp** inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero).

## <a name="syntax"></a>Sintaxe


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

As páginas de ajuda da Web sempre contêm as informações mais recentes e mais detalhadas sobre erros do Windows Media Player. Esse método transfere automaticamente as outras informações necessárias pela ajuda da Web, como a versão do sistema operacional que está sendo usada.

Para acessar as páginas de ajuda da Web diretamente, use os seguintes links de código de erro e centro de suporte:

-   [Informações de código de erro do Windows Media Player](https://support.microsoft.com/kb/886273)
-   [Centro de soluções do Windows Media Player](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um botão que inicia a página de ajuda da Web do Microsoft Windows Media Player no navegador. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





