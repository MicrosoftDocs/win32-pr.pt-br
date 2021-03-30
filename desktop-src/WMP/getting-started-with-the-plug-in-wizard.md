---
title: Introdução com o assistente de plug-in
description: Introdução com o assistente de plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Plug-ins do Windows Media Player, instalando o assistente de plug-in
- plug-ins, instalando o assistente de plug-in
- Criando plug-ins, instalando o assistente de plug-in
- Assistente de plug-in do Windows Media Player, instalando
- Instalando o assistente de plug-in
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916480"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Introdução com o assistente de plug-in

Para configurar seu ambiente de desenvolvimento para a criação de plug-ins do Windows Media Player, você deve instalar os seguintes itens:

-   Microsoft Visual Studio .NET 2003 ou posterior
-   Windows Media Player 9 Series ou posterior
-   SDK do Windows, que inclui o SDK do Windows Media Player
-   Assistente de plug-in do Windows Media Player

## <a name="installing-the-wizard"></a>Instalando o assistente

Execute as etapas a seguir para instalar o assistente de plug-in do Windows Media Player.

1.  Localize a pasta onde você instalou o SDK do Windows. Expanda a pasta para exibir suas subpastas e navegue até exemplos \\ \\ assistentes de WMP multimídia \\ \\ wmpwiz.
2.  Localize os três arquivos a seguir:
    -   wmpwiz. vsz
    -   wmpwiz. vsdir
    -   wmpwiz. ico
3.  Usando um editor de texto, como o bloco de notas, edite o arquivo wmpwiz. vsz.

    Localize a seguinte linha:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Altere `<VsWizardEngine version goes here>` para um dos valores a seguir, dependendo da versão do Visual Studio instalada.

    

    | Valor              | Versão do Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine. 7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine. 8.0 | Visual Studio 2005      |
    | VsWizardEngine. 9.0 | Visual Studio 2008      |

    

     

    Localize a seguinte linha:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Altere `<path to wmpwiz directory goes here>` para o caminho onde os arquivos do assistente estão localizados.

    Por exemplo, suponha que você tenha o Visual Studio 2008 e que os arquivos do assistente estejam aqui: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WMP \\ assistentes \\ wmpwiz. Em seguida, o arquivo wmpwiz. vsz teria esta aparência:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Localize a pasta onde você instalou o Visual Studio. Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.
5.  Copie os três arquivos listados na etapa 2 para a pasta vcprojects. O assistente agora está instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um plug-in](building-a-plug-in.md)
</dt> <dt>

[Usando o assistente de plug-in com o Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




