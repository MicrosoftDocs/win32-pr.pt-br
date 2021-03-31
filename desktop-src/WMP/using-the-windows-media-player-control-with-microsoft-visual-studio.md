---
title: Usando o controle do Windows Media Player com Microsoft Visual Studio
description: Usando o controle do Windows Media Player com Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player,. NET Framework
- Modelo de objeto do Windows Media Player,. NET Framework
- modelo de objeto,. NET Framework
- Windows Media Player Mobile, .NET Framework
- Controle ActiveX do Windows Media Player, .NET Framework
- Controle ActiveX móvel do Windows Media Player, .NET Framework
- Controle ActiveX, .NET Framework
- Controle ActiveX do Windows Media Player, Visual Studio
- Controle ActiveX móvel do Windows Media Player, Visual Studio
- Controle ActiveX, Visual Studio
- .NET Framework, incorporação de programa do Visual Studio
- incorporando, programas do Visual Studio
- Visual Studio, incorporação de programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104006221"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Usando o controle do Windows Media Player com Microsoft Visual Studio

Você pode adicionar o controle ActiveX do Windows Media Player 9 Series ou posterior a um aplicativo .NET Framework por meio da caixa de ferramentas no Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Adicionando o controle do Windows Media Player

Antes de criar um novo projeto, verifique se a versão mais recente do Windows Media Player e o SDK do Windows Media Player estão instalados no computador.

Inicie o Visual Studio e crie um novo projeto.

No Visual Studio, abra a caixa de ferramentas.

Se o Windows Media Player não aparecer na parte **componentes** da caixa de ferramentas, faça o seguinte:

1.  Clique com o botão direito do mouse na caixa de ferramentas e selecione **escolher itens**. Isso abre a caixa de diálogo Personalizar caixas de **ferramentas** .
2.  Na guia **componentes com** , selecione Windows Media Player.

    Se o Windows Media Player não aparecer na lista, clique em **procurar** e abra Wmp.dll, que deve estar na pasta system32 do Windows \\ .

3.  Clique em **OK**. O controle do Windows Media Player será colocado na guia atual da caixa de ferramentas.

Agora você pode selecionar o Windows Media Player na caixa de ferramentas e adicioná-lo a um formulário.

O Visual Studio dá ao controle do Windows Media Player um nome padrão, como "axWindowsMediaPlayer1". Talvez você queira alterar o nome para algo mais facilmente lembrado, como "Player".

Adicionar o controle do Windows Media Player da caixa de ferramentas também adiciona referências a duas bibliotecas criadas pelo Visual Studio, AxWMPLib e WMPLib. Você pode encontrá-los na Gerenciador de Soluções em **referências**.

Para facilitar o uso dos objetos no namespace do Player, você deve incluir o namespace nas diretivas using ou Imports de seus arquivos, da seguinte maneira:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



A diretiva garante que você possa consultar objetos do **Player** sem qualificar totalmente seus nomes.

> [!Note]  
> O controle do Windows Media Player é um objeto **AxWindowsMediaPlayer** do namespace **AxWMPLib** . No entanto, a classe **AxWindowsMediaPlayer** usa tipos de dados, interfaces e outros elementos do namespace **WMPLib** .

 

## <a name="configuring-visibility-of-the-control"></a>Configurando a visibilidade do controle

Quando você adiciona o controle do Windows Media Player pela primeira vez a um formulário, ele ficará visível. Se você não quiser usar a imagem visível do Player em seu aplicativo, oculte o player padrão definindo qualquer uma das seguintes propriedades:



| Propriedade        | Valor                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "invisível" (consulte [Player. UIMODE](player-uimode.md).) |
| **Visível**     | "false"                                               |
| **Tamanho. largura**  | 0                                                     |
| **Tamanho. altura** | 0                                                     |



 

Você pode definir essas propriedades no código ou na janela **Propriedades** quando o controle do Windows Media Player é selecionado no designer de formulário.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilidade do modelo de objeto do controle

O modelo de objeto para o controle do Windows Media Player é basicamente o mesmo na .NET Framework como em código e script não gerenciados. No entanto, há diferenças em como os elementos são expostos:

-   A maioria dos objetos é exposta sob o nome da interface COM subjacente. Por exemplo, o objeto **playlist** é exposto como **IWMPPlaylist**.
-   Algumas interfaces têm versões posteriores. Por exemplo, **IWMPMedia** recebeu funcionalidade adicional em **IWMPMedia2** e **IWMPMedia3**. Se você declarar um objeto como **IWMPMedia**, normalmente terá acesso à funcionalidade de todas as versões da interface. No entanto, o IntelliSense® não reconhecerá os métodos ou as propriedades das interfaces de versão posteriores, e o Editor Visual Basic .NET não corrigirá automaticamente a capitalização. Para obter o benefício completo do IntelliSense e de outros recursos do Visual Studio, declare o objeto usando a versão mais recente da interface, como **IWMPMedia3**.
-   Não há propriedades indexadas (C#) ou propriedades padrão (Visual Basic .NET). Por exemplo, para recuperar um **playlist. Item**, você deve chamar o método acessador **IWMPlaylist. get \_ Item** em C# ou recuperar a propriedade **IWMPlayist. Item** no Visual Basic .net.
-   Devido a um conflito de nomenclatura entre a propriedade de **controles** do Windows Media Player e a propriedade **Controls** exposta por cada controle, a versão do Player dessa propriedade é chamada de **CtlControls** no contexto do controle ActiveX. (No entanto, esse não é o caso quando você cria o Player programaticamente, em vez de um controle ActiveX.)

Use o pesquisador de objetos no Visual Studio para localizar os nomes de API corretos para métodos e objetos nos namespaces **AxWMPLib** e **WMPLib** .

## <a name="distributing-your-application"></a>Distribuindo o aplicativo

Ao distribuir seu aplicativo, certifique-se de instalar AxInterop.WMPLib.dll e Interop.WMPLib.dll na pasta do aplicativo. Você também precisará certificar-se de que a versão necessária do Windows Media Player esteja instalada no computador do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o controle do Windows Media Player programaticamente**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Inserindo o controle do Windows Media Player em uma solução C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Inserindo o controle do Windows Media Player em uma solução Visual Basic .NET**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




