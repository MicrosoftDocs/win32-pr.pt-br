---
title: Instalando o assistente de plug-in da loja online
description: Instalando o assistente de plug-in da loja online
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Repositórios online do Windows Media Player, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 1 lojas online, assistente de plug-in
- Armazenamentos online do Windows Media Player, instalando o assistente de plug-in
- lojas online, instalando o assistente de plug-in
- Digite 1 lojas online, instalando o assistente de plug-in
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, instalando o assistente de plug-in
- plug-ins, assistente de plug-in
- Plug-ins do Windows Media Player, tipo 1 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, instalando o assistente de plug-in
- Plug-ins do Windows Media Player, assistente de plug-in
- Instalando o assistente de plug-in
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005633"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Instalando o assistente de plug-in da loja online

Para configurar seu ambiente de desenvolvimento para criar plug-ins de loja online do tipo 1, você deve instalar os seguintes itens:

-   Microsoft Visual Studio 2005 ou posterior
-   Windows Media Player 11 ou posterior
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

    

    | Valor              | Versão do Visual Studio |
    |--------------------|-----------------------|
    | VsWizardEngine. 8.0 | Visual Studio 2005    |
    | VsWizardEngine. 9.0 | Visual Studio 2008    |

    

     

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

[Criando o plug-in para uma loja online tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




