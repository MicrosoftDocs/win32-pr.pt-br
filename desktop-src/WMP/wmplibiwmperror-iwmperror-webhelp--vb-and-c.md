---
title: Método webHelp IWMPError
description: O método webHelp inicia a página Windows Media Player Web Help para exibir mais informações sobre o primeiro erro na fila de erros (índice zero). | Método webHelp IWMPError
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- Método webHelp Windows Media Player
- método webHelp Windows Media Player interface , IWMPError
- Interface IWMPError Windows Media Player , método webHelp
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
ms.openlocfilehash: 50d4b404988e8b317ec7b090adcb96aac8e26a5a82590aa1138848dc797e3e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115819"
---
# <a name="iwmperrorwebhelp-method"></a>Método IWMPError::webHelp

O **método webHelp** inicia a página Windows Media Player Web Help para exibir mais informações sobre o primeiro erro na fila de erros (índice zero).

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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

As páginas da Ajuda da Web sempre contêm as informações mais recentes e detalhadas sobre Windows Media Player erros. Esse método transfere automaticamente as outras informações necessárias para a Ajuda da Web, como a versão do sistema operacional que está sendo usada.

Para acessar as páginas da Ajuda da Web diretamente, use o seguinte código de erro e links do centro de suporte:

-   [Windows Media Player Informações de código de erro](https://support.microsoft.com/kb/886273)
-   [Windows Media Player Centro de Soluções](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um botão que inicia a página Windows Media Player Ajuda da Web da Microsoft no navegador. O objeto AxWMPLib.AxWindowsMediaPlayer é representado pela variável chamada player.


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
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





