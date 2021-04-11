---
title: Usando o controle do Windows Media Player com Visual Basic
description: Usando o controle do Windows Media Player com Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, Visual Basic
- Modelo de objeto do Windows Media Player, Visual Basic
- modelo de objeto, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Controle ActiveX do Windows Media Player, Visual Basic
- Controle ActiveX móvel do Windows Media Player, Visual Basic
- Controle ActiveX, Visual Basic
- Incorporação de programas baseados em Visual Basic
- incorporação, programas baseados em Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292398"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>Usando o controle do Windows Media Player com Visual Basic

Esta seção descreve como usar o controle ActiveX do Windows Media Player 9 Series ou posterior em aplicativos criados com o Microsoft Visual Basic 6,0.

## <a name="getting-started"></a>Introdução

Para adicionar o controle do Windows Media Player à caixa de ferramentas, primeiro selecione **componentes** no menu **projeto** . Na caixa de diálogo componentes, marque a caixa de seleção ao lado de "Windows Media Player". Na parte inferior da caixa de diálogo, confirme se o arquivo selecionado está wmp.dll. Depois de fechar a caixa de diálogo, você pode colocar uma instância do controle do Windows Media Player no formulário de maneira usual.

Você pode definir muitas propriedades de controle usando o janela Propriedades. Para definir algumas propriedades, você deve usar a caixa de diálogo Propriedades do Windows Media Player, que você abre usando o item "(personalizado)" no janela Propriedades.

## <a name="object-references"></a>Referências de objeto

Você usa determinadas propriedades de controle do Player para obter referências a objetos específicos. Por exemplo, a propriedade **cdromCollection** retorna uma referência a um objeto **cdromCollection** . Você deve atribuir tal referência a uma variável que você declarou como a interface correspondente. No caso da propriedade **cdromCollection** , por exemplo, você atribui seu valor de retorno a uma variável do tipo **IWMPCdromCollection**.

Leia o tópico [interfaces](interfaces.md) na [referência do modelo de objeto para C++](object-model-reference-for-c.md) para identificar quais objetos implementam várias interfaces. Nesses casos, você deve declarar uma variável de objeto como a interface de numeração mais alta documentada neste SDK para ter acesso a todas as propriedades e métodos desse objeto. Por exemplo, você deve atribuir o valor da propriedade **currentMedia** de controle do Windows Media Player a uma variável declarada como **IWMPMedia3** para garantir que você tenha acesso aos métodos **getAttributeCountByType** e **getItemInfoByType** .

> [!Note]  
> O objeto **WindowsMediaPlayer** implementa todas as propriedades e métodos das interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** e **IWMPPlayer4** . Você não precisa declarar variáveis separadas para qualquer uma dessas interfaces. Você pode acessar todos os seus membros usando o nome que você atribuiu à sua instância do **WindowsMediaPlayer** .

 

No Pesquisador de objetos do Visual Basic, você verá muitas interfaces destinadas ao uso privado pelo controle do Windows Media Player, incluindo algumas que dão suporte a desenvolvedores de capas. Você deve usar somente os objetos, as propriedades, os métodos e os eventos documentados neste SDK.

## <a name="additional-tips"></a>Dicas Adicionais

-   A documentação de referência mostra a sintaxe do JScript. No JScript, os argumentos passados para os métodos são sempre colocados entre parênteses. No Visual Basic 6,0, os argumentos passados para métodos que não retornam um valor não devem ser colocados entre parênteses.
-   Algumas propriedades ou métodos podem não aparecer no recurso de conclusão de código de lista automática no editor de código de Visual Basic. Você ainda pode usar esses membros digitando seus nomes exatamente como aparecem nesta documentação.
-   Gerencie a aparência visual do controle usando a propriedade **UIMODE** . Você pode fazer isso de duas maneiras. Você pode usar a lista suspensa **selecionar um modo** na caixa de diálogo Propriedades do Windows Media Player ou pode digitar o valor correto no janela Propriedades.

    Em particular, não use a propriedade **Visible** para ocultar o controle; em vez disso, atribua o valor "invisível" à propriedade **UIMODE** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de controle do Player**](player-control-guide.md)
</dt> </dl>

 

 




