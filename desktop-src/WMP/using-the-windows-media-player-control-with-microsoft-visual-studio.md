---
title: Usando o controle Windows Media Player com Microsoft Visual Studio
description: Usando o controle Windows Media Player com Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, incorporando ActiveX controle
- Windows Media Player modelo de objeto, incorporando ActiveX controle
- modelo de objeto, incorporando ActiveX controle
- Windows Media Player Mobile, incorporando ActiveX controle
- Windows Media Player ActiveX controle,incorporação
- Windows Media Player Controle ActiveX dispositivo móvel, incorporação
- ActiveX controle,incorporação
- Windows Media Player,.NET Framework
- Windows Media Player modelo de objeto,.NET Framework
- modelo de objeto, .NET Framework
- Windows Media Player Mobile,.NET Framework
- Windows Media Player ActiveX controle,.NET Framework
- Windows Media Player Controle ActiveX dispositivo móvel, .NET Framework
- ActiveX controle,.NET Framework
- Windows Media Player ActiveX controle,Visual Studio
- Windows Media Player Controle ActiveX dispositivo móvel, Visual Studio
- ActiveX controle,Visual Studio
- .NET Framework,Visual Studio de programação
- incorporação, Visual Studio programas
- Visual Studio,incorporação de programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bb9597b8ad5baadbd51625c68a1d7fb7ebc1791c2d6e8015fb79ba2cab3be6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830445"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Usando o controle Windows Media Player com Microsoft Visual Studio

Você pode adicionar o controle Windows Media Player Série 9 ou posterior ActiveX a um aplicativo .NET Framework por meio da Caixa de Ferramentas Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Adicionando o Windows Media Player controle

Antes de criar um novo projeto, certifique-se de que a versão mais recente do Windows Media Player e do SDK do Windows Media Player está instalada em seu computador.

Inicie Visual Studio e, em seguida, crie um novo projeto.

No Visual Studio, abra a Caixa de Ferramentas.

Se Windows Media Player não aparecer na **parte** Componentes da Caixa de Ferramentas, faça o seguinte:

1.  Clique com o botão direito do mouse na Caixa de Ferramentas e selecione **Escolher Itens**. Isso abre a **caixa de diálogo Personalizar Caixa** de Ferramentas.
2.  Na guia **Componentes COM,** selecione Windows Media Player.

    Se Windows Media Player aparecer na lista, clique em Procurar **e** abra Wmp.dll, que deve estar na pasta Windows \\ System32.

3.  Clique em **OK**. O Windows Media Player controle será colocado na guia Caixa de Ferramentas atual.

Agora você pode selecionar Windows Media Player na Caixa de Ferramentas e adicioná-lo a um formulário.

Visual Studio dá ao Windows Media Player um nome padrão, como "axWindowsMediaPlayer1". Talvez você queira alterar o nome para algo mais facilmente lembrado, como "Player".

Adicionar o Windows Media Player controle da Caixa de Ferramentas também adiciona referências a duas bibliotecas criadas por Visual Studio, AxWMPLib e WMPLib. Você pode encontrá-los no Gerenciador de Soluções em **Referências**.

Para facilitar o uso dos objetos no namespace player, você deve incluir o namespace nas diretivas using ou imports de seus arquivos, da seguinte maneira:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



A diretiva garante que você possa se referir a **objetos player** sem qualificar totalmente seus nomes.

> [!Note]  
> O Windows Media Player controle é um **objeto AxWindowsMediaPlayer** do namespace **AxWMPLib.** No entanto, **a classe AxWindowsMediaPlayer** usa tipos de dados, interfaces e outros elementos do namespace **WMPLib.**

 

## <a name="configuring-visibility-of-the-control"></a>Configurando a visibilidade do controle

Quando você adicionar o controle Windows Media Player a um formulário pela primeira vez, ele ficará visível. Se você não quiser usar a imagem visível do Player em seu aplicativo, o ocultará o Player padrão definindo qualquer uma das seguintes propriedades:



| Propriedade        | Valor                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "invisível" (consulte [Player.uiMode](player-uimode.md).) |
| **Visível**     | "false"                                               |
| **Size.Width**  | 0                                                     |
| **Size.Height** | 0                                                     |



 

Você pode definir essas propriedades no código ou na **janela Propriedades** quando o controle Windows Media Player é selecionado no designer de formulário.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilidade do modelo de objeto do controle

O modelo de objeto para o Windows Media Player controle é basicamente o mesmo no .NET Framework como no código e no script não controlados. No entanto, há diferenças em como os elementos são expostos:

-   A maioria dos objetos é exposta sob o nome de sua interface COM subjacente. Por exemplo, o **objeto Playlist** é exposto como **IWMPPlaylist.**
-   Algumas interfaces têm versões posteriores. Por exemplo, **O IWMPMedia** recebeu funcionalidade adicional em **IWMPMedia2** e **IWMPMedia3.** Se você declarar um objeto como **IWMPMedia**, geralmente terá acesso à funcionalidade de todas as versões da interface. No entanto, o IntelliSense® não reconhecerá os métodos ou as propriedades das interfaces de versão posterior, e o editor Visual Basic .NET não corrigirá automaticamente a capitalização. Para obter o benefício completo do IntelliSense e outros recursos do Visual Studio, declare o objeto usando a versão mais recente da interface, como **IWMPMedia3**.
-   Não há propriedades indexadas (C#) ou propriedades padrão (Visual Basic .NET). Por exemplo, para recuperar um **Playlist.item**, você deve chamar o método de acessador de **\_ item IWMPlaylist.get** em C# ou recuperar a propriedade **IWMPlayist.Item** no Visual Basic .NET.
-   Devido a um conflito de nomen entre a propriedade Windows Media Player **Controls** e a propriedade **Controls** exposta por cada controle, a versão do Player dessa propriedade é chamada **CtlControls** no contexto do controle ActiveX controle. (No entanto, esse não é o caso quando você cria o Player programaticamente em vez de como um ActiveX controle.)

Use o Pesquisador de Objetos Visual Studio para localizar os nomes de API corretos para métodos e objetos nos namespaces **AxWMPLib** e **WMPLib.**

## <a name="distributing-your-application"></a>Distribuindo o aplicativo

Ao distribuir seu aplicativo, certifique-se de instalar AxInterop.WMPLib.dll e Interop.WMPLib.dll na pasta do aplicativo. Você também precisará certificar-se de que a versão Windows Media Player necessária está instalada no computador do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o controle Windows Media Player programaticamente**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Incorporação do controle Windows Media Player em uma solução C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Incorporação do controle Windows Media Player em uma solução Visual Basic .NET**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




