---
title: Instalando o assistente de projeto
description: Instalando o assistente de projeto
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 2 lojas online, plug-ins
- Repositórios online do Windows Media Player, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 2 lojas online, assistente de plug-in
- Lojas online do Windows Media Player, assistente de projeto
- lojas online, assistente de projeto
- tipo 2 lojas online, assistente de projeto
- Armazenamentos online do Windows Media Player, instalando o assistente de plug-in
- lojas online, instalando o assistente de plug-in
- tipo 2 lojas online, instalando o assistente de plug-in
- Armazenamentos online do Windows Media Player, assistente de instalação de projeto
- repositórios online, assistente de instalação de projeto
- tipo 2 lojas online, assistente de instalação de projeto
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, tipo 2 lojas online
- plug-ins, instalando o assistente de plug-in
- plug-ins, assistente de plug-in
- plug-ins, assistente de instalação de projeto
- plug-ins, assistente de projeto
- Plug-ins do Windows Media Player, tipo 2 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, instalando o assistente de plug-in
- Plug-ins do Windows Media Player, assistente de plug-in
- Plug-ins do Windows Media Player, assistente para instalação de projeto
- Plug-ins do Windows Media Player, assistente de projeto
- Instalando o assistente de plug-in
- Assistente de plug-in
- Assistente de instalação de projeto
- Assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636398"
---
# <a name="installing-the-project-wizard"></a>Instalando o assistente de projeto

Para configurar seu ambiente de desenvolvimento para criar plug-ins de loja online do tipo 2, você deve instalar os seguintes itens:

-   Microsoft Visual Studio .NET 2003 ou posterior
-   Windows Media Player 9 Series ou posterior
-   SDK do Windows, que inclui o SDK do Windows Media Player
-   Assistente de plug-in da loja online

## <a name="installing-the-wizard"></a>Instalando o assistente

Use as etapas a seguir para instalar o assistente de plug-in da loja online no Visual Studio.

1.  Localize a pasta onde você instalou o SDK do Windows. Expanda a pasta para exibir suas subpastas e navegue até exemplos \\ \\ serviços de assistentes de WMP de multimídia \\ \\ .
2.  Localize os três arquivos a seguir:
    -   wmpservices. vsz
    -   wmpservices. vsdir
    -   wmpservices. ico
3.  Usando um editor de texto como o bloco de notas, edite o arquivo wmpservices. vsz.

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
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Altere `<path to wmpservices directory goes here>` para o caminho onde os arquivos do assistente estão localizados.

    Por exemplo, suponha que você tenha o Visual Studio 2008 e que os arquivos do assistente estejam aqui: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WMP \\ assistentes \\ serviços. Em seguida, o arquivo wmpservices. vsz teria esta aparência:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Localize a pasta onde você instalou o Visual Studio. Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.
5.  Copie os três arquivos listados na etapa 2 para a pasta vcprojects. O assistente agora está instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o plug-in para uma loja online tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




