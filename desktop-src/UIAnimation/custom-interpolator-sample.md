---
title: Exemplo de Interpolador Personalizado
description: Mostra como usar a animação Windows com seu próprio Interpolador Personalizado, com Direct2D usado para renderização.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c801822bd50eebe9f405cad00bc8ffcd7ac2d611924a3ff0bae91d30bc9f249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999696"
---
# <a name="custom-interpolator-sample"></a>Exemplo de Interpolador Personalizado

Mostra como usar a animação Windows com seu próprio Interpolador Personalizado, com Direct2D usado para renderização. As imagens de exemplo são carregadas da Biblioteca de Imagens.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Localização                               | Caminho/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galeria de código                           | [Windows Código de exemplo do Gerenciador de Animação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação. Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para Windows 7, os exemplos serão instalados em C: Arquivos de Programas \\ \\ SDKs da Microsoft Windows \\ \\ exemplos v7.0. \\

## <a name="building-the-sample"></a>Compilando o exemplo

Use um dos métodos a seguir para criar o exemplo.

**Para criar o exemplo no prompt de comando**

1.  Abra a janela Prompt de Comando e navegue até o diretório do projeto CustomInterpolator. Por exemplo, o caminho de instalação padrão para este exemplo é C: Arquivos de \\ \\ Programas Microsoft SDKs \\ Windows \\ v7.0 \\ Exemplos multimídia \\ \\ WindowsAnimation \\ CustomInterpolator

2.  Execute o seguinte comando: **msbuild CustomInterpolator.sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra Windows Explorer e navegue até o diretório do projeto CustomInterpolator.

    > [!Note]  
    > A extensão de nome de arquivo .sln não é mostrada nas configurações de pasta padrão. Nessa situação, ele pode ser identificado por seu ícone exclusivo ou por sua descrição de tipo, "Microsoft Visual Studio Solução".

     

2.  Clique duas vezes no ícone do arquivo CustomInterpolator.sln para abrir o projeto Visual Studio.

3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável usando o prompt de comando ou Windows Explorer.

2.  Execute **CustomInterpolator.exe** no prompt de comando ou clique duas vezes no ícone para CustomInterpolator.exe no Windows Explorer.
3.  Reesize a janela ou pressione a barra de espaços e as imagens se organizarão aleatoriamente no meio da área do cliente.

4.  Pressione a seta para cima ou para baixo e as imagens serão aceleradas na parte superior ou inferior da área do cliente.

 

 




