---
title: Ponto de Partida com o Assistente de Plug-in
description: Ponto de Partida com o Assistente de Plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Windows Media Player plug-ins, instalando o assistente de plug-in
- plug-ins, assistente de instalação de plug-in
- criando plug-ins, instalando o assistente de plug-in
- Windows Media Player Assistente de plug-in, instalação
- instalando o assistente de plug-in
- assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2699d0316be93f6387bdc64c6671df868eaa70fb24a4ad3619026524106432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576575"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Ponto de Partida com o Assistente de Plug-in

Para configurar seu ambiente de desenvolvimento para Windows Media Player plug-ins, você deve instalar os seguintes itens:

-   Microsoft Visual Studio .NET 2003 ou posterior
-   Windows Media Player série 9 ou posterior
-   Windows SDK, que inclui o Windows Media Player SDK
-   Windows Media Player Assistente de plug-in

## <a name="installing-the-wizard"></a>Instalando o Assistente

Execute as etapas a seguir para instalar o assistente Windows Media Player plug-in.

1.  Localize a pasta em que você instalou Windows SDK. Expanda a pasta para exibir suas subpastas e navegue até Assistentes WMP multimídia \\ \\ de \\ \\ exemplos wmpwiz.
2.  Localize os três arquivos a seguir:
    -   wmpwiz.vsz
    -   wmpwiz.vsdir
    -   wmpwiz.ico
3.  Usando um editor de texto, como Bloco de notas, edite o arquivo wmpwiz.vsz.

    Localize a seguinte linha:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Altere `<VsWizardEngine version goes here>` para um dos valores a seguir, dependendo de qual versão Visual Studio você instalou.

    

    | Valor              | Versão do Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Localize a seguinte linha:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Altere `<path to wmpwiz directory goes here>` para o caminho onde os arquivos do assistente estão localizados.

    Por exemplo, suponha que você tenha Visual Studio 2008 e seus arquivos de assistente estão aqui: C: Arquivos de Programas \\ \\ SDKs da Microsoft Windows \\ \\ v7.0 \\ \\ \\ Exemplos assistentes WMP multimídia \\ \\ wmpwiz. Em seguida, o arquivo wmpwiz.vsz teria esta aparência:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Localize a pasta onde você instalou Visual Studio. Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.
5.  Copie os três arquivos listados na etapa 2 para a pasta vcprojects. O assistente agora está instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um plug-in](building-a-plug-in.md)
</dt> <dt>

[Usando o Assistente de Plug-in com Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




