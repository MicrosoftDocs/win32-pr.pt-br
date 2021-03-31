---
title: Inserindo o controle do Windows Media Player em um programa personalizado
description: Inserindo o controle do Windows Media Player em um programa personalizado
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Windows Media Player Mobile, inserindo controle ActiveX
- incorporação, programas personalizados
- inserção de programa personalizada
- incorporação, programas baseados em Visual Basic
- Incorporação de programas baseados em Visual Basic
- inserindo, manualmente usando métodos COM
- inserção manual usando métodos COM
- incorporando, programas em C++
- Incorporação de programa C++
- incorporando, programas do Visual Studio
- Visual Studio, incorporação de programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005294"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>Inserindo o controle do Windows Media Player em um programa personalizado

Como o controle ActiveX do Windows Media Player é baseado na tecnologia Microsoft Component Object Model (COM), você pode incorporá-lo em programas escritos com muitas linguagens de programação diferentes. O controle do Windows Media Player representa uma maneira fácil de adicionar uma funcionalidade de mídia digital sofisticada a qualquer programa.

No Microsoft Visual Basic, você pode adicionar o controle à caixa de ferramentas de controle, colocá-lo em um formulário e ajustar as propriedades de controle na janela Propriedades. Se você quiser uma interface de usuário personalizada, poderá posicionar os botões de comando no formulário e adicionar o código que gerencia o controle do Windows Media Player. A inserção do controle em um programa baseado em Visual Basic é muito semelhante a incorporá-lo em um documento do Office e sua programação com o VBA.

Como alternativa, você pode inserir o controle manualmente usando métodos COM para instanciar o controle e acessar as interfaces COM documentadas em [referência de modelo de objeto para C++](object-model-reference-for-c.md).

Ao inserir o controle do Windows Media Player em um programa C++, você tem a opção de implementar interfaces COM que permitem que o controle seja executado no modo remoto. Isso significa que o controle incorporado compartilha o mesmo mecanismo de reprodução que o modo completo do Player, e os usuários podem alternar entre o modo completo e o estado encaixado sem interromper a reprodução de mídia digital. Você também pode controlar o que é exibido nos vários painéis do player de modo completo quando os usuários alternam para o estado desencaixado.

Com a incorporação de C++, você também tem a opção de aplicar um arquivo de definição de capa ao controle do player incorporado. Essa é uma maneira fácil de criar um código de interface de usuário leve que você pode manter separadamente do código do programa principal.

O Microsoft Visual Studio dá suporte à inserção de controles ActiveX, incluindo o controle do Windows Media Player. Quando você opta por fazer isso, o Visual Studio cria um novo assembly de interoperabilidade alternativo (Interop) para gerenciar a interoperabilidade entre o .NET Framework e o controle do Windows Media Player. O Visual Studio usa a ferramenta de tlbimp.exe de .NET Framework para criar o assembly de interoperabilidade. Isso significa que as assinaturas exibidas ao usar o recurso IntelliSense no Visual Studio usam semântica determinada pela versão atual do Tlbimp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Inserindo o controle do Windows Media Player**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**Usando o controle do Windows Media Player em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**Usando o controle do Windows Media Player em uma solução de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Usando o controle do Windows Media Player com Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




