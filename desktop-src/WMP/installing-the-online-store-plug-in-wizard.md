---
title: Instalando o assistente de plug-in da loja online
description: Instalando o assistente de plug-in da loja online
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player lojas online, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Windows Media Player repositórios online, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 1 lojas online, assistente de plug-in
- Windows Media Player lojas online, instalando o assistente de plug-in
- lojas online, instalando o assistente de plug-in
- Digite 1 lojas online, instalando o assistente de plug-in
- plug-ins, Windows Media Player lojas online
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, instalando o assistente de plug-in
- plug-ins, assistente de plug-in
- plug-ins Windows Media Player, tipo 1 lojas online
- plug-ins Windows Media Player, lojas online
- Windows Media Player plug-ins, Windows Media Player lojas online
- plug-ins Windows Media Player, instalando o assistente de plug-in
- plug-ins Windows Media Player, assistente de plug-in
- Instalando o assistente de plug-in
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1088d915715be44de092604d626bc24792f6d263a9765a1076ce1afa3f67ef4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135539"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Instalando o assistente de plug-in da loja online

Para configurar seu ambiente de desenvolvimento para criar plug-ins de loja online do tipo 1, você deve instalar os seguintes itens:

-   Microsoft Visual Studio 2005 ou posterior
-   Windows Media Player 11 ou posterior
-   Windows sdk, que inclui o sdk do Windows Media Player
-   Assistente de plug-in da loja online

## <a name="installing-the-wizard"></a>Instalando o assistente

Use as etapas a seguir para instalar o assistente de plug-in da loja online no Visual Studio.

1.  localize a pasta onde você instalou o SDK do Windows. Expanda a pasta para exibir suas subpastas e navegue até exemplos \\ \\ serviços de assistentes de WMP de multimídia \\ \\ .
2.  Localize os três arquivos a seguir:
    -   wmpservices. vsz
    -   wmpservices. vsdir
    -   wmpservices. ico
3.  usando um editor de texto como Bloco de notas, edite o arquivo wmpservices. vsz.

    Localize a seguinte linha:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    altere `<VsWizardEngine version goes here>` para um dos valores a seguir, dependendo da versão do Visual Studio que você instalou.

    

    | Valor              | Versão do Visual Studio |
    |--------------------|-----------------------|
    | VsWizardEngine. 8.0 | Visual Studio 2005    |
    | VsWizardEngine. 9.0 | Visual Studio 2008    |

    

     

    Localize a seguinte linha:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Altere `<path to wmpservices directory goes here>` para o caminho onde os arquivos do assistente estão localizados.

    por exemplo, suponha que você tenha Visual Studio 2008 e que os arquivos do assistente estejam aqui: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WMP \\ assistentes \\ serviços. Em seguida, o arquivo wmpservices. vsz teria esta aparência:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Localize a pasta onde você instalou Visual Studio. Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.
5.  Copie os três arquivos listados na etapa 2 para a pasta vcprojects. O assistente agora está instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando o plug-in para uma loja online tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




