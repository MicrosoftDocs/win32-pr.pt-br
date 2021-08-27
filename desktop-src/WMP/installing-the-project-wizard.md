---
title: Instalando o assistente Project aplicativo
description: Instalando o assistente Project aplicativo
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player lojas online, plug-ins
- lojas online, plug-ins
- tipo 2 lojas online, plug-ins
- Windows Media Player online, assistente de plug-in
- lojas online, assistente de plug-in
- tipo 2 lojas online, assistente de plug-in
- Windows Media Player online, assistente de projeto
- lojas online, assistente de projeto
- type 2 online stores,project wizard
- Windows Media Player online, instalando o assistente de plug-in
- lojas online, assistente de instalação de plug-in
- tipo 2 lojas online, assistente de instalação de plug-in
- Windows Media Player online, instalando o assistente de projeto
- lojas online, assistente de instalação de projeto
- tipo 2 lojas online, assistente de instalação de projeto
- plug-ins, Windows Media Player online
- plug-ins, lojas online
- plug-ins, tipo 2 lojas online
- plug-ins, assistente de instalação de plug-in
- plug-ins, assistente de plug-in
- plug-ins, assistente de instalação de projeto
- plug-ins, assistente de projeto
- Windows Media Player plug-ins, digite 2 lojas online
- Windows Media Player plug-ins, lojas online
- Windows Media Player plug-ins, Windows Media Player online
- Windows Media Player plug-ins, instalando o assistente de plug-in
- Windows Media Player plug-ins, assistente de plug-in
- Windows Media Player plug-ins, instalando o assistente de projeto
- Windows Media Player plug-ins, assistente de projeto
- instalando o assistente de plug-in
- assistente de plug-in
- instalando o assistente de projeto
- assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f00e0430791fb36285ba365eed752083889f2b55bd126c4a588d2a506f58acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123516"
---
# <a name="installing-the-project-wizard"></a>Instalando o assistente Project aplicativo

Para configurar seu ambiente de desenvolvimento para criar plug-ins de lojas online do tipo 2, você deve instalar os seguintes itens:

-   Microsoft Visual Studio .NET 2003 ou posterior
-   Windows Media Player série 9 ou posterior
-   Windows SDK, que inclui o Windows Media Player SDK
-   Assistente de plug-in da loja online

## <a name="installing-the-wizard"></a>Instalando o Assistente

Use as etapas a seguir para instalar o assistente de plug-in da loja online Visual Studio.

1.  Localize a pasta em que você instalou Windows SDK. Expanda a pasta para exibir suas subpastas e navegue até Exemplos Serviços de \\ \\ assistentes WMP \\ \\ multimídia.
2.  Localize os três arquivos a seguir:
    -   wmpservices.vsz
    -   wmpservices.vsdir
    -   wmpservices.ico
3.  Usando um editor de texto como Bloco de notas, edite o arquivo wmpservices.vsz.

    Localize a seguinte linha:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Altere `<VsWizardEngine version goes here>` para um dos valores a seguir, dependendo de qual versão do Visual Studio você instalou.

    

    | Valor              | Versão do Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Localize a seguinte linha:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Altere `<path to wmpservices directory goes here>` para o caminho onde os arquivos do assistente estão localizados.

    Por exemplo, suponha que você tenha Visual Studio 2008 e seus arquivos de assistente estão aqui: C: Arquivos de Programas SDKs da Microsoft Windows serviços de assistentes WMP multimídia de \\ \\ \\ \\ exemplos v7.0. \\ \\ \\ \\ \\ Em seguida, o arquivo wmpservices.vsz teria esta aparência:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Localize a pasta na qual você instalou Visual Studio. Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.
5.  Copie os três arquivos listados na etapa 2 para a pasta vcprojects. O assistente agora está instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o plug-in para uma loja online do tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




