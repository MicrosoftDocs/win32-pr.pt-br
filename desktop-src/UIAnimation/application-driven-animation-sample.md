---
title: Application-Driven de animação
description: Mostra Windows animação na configuração controlada por aplicativo usando Direct2D para animar a cor da tela de fundo de uma janela e sincronizar com a taxa de atualização.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfbb5ce71ddeff6a37c2d872e0e1e93fdc58cde9fcc8359560d9d386ba7a0834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137369"
---
# <a name="application-driven-animation-sample"></a>Application-Driven de animação

Mostra Windows animação na configuração controlada por aplicativo usando Direct2D para animar a cor da tela de fundo de uma janela e sincronizar com a taxa de atualização.

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

1.  Abra a janela Prompt de Comando e navegue até o diretório do projeto AppDriven. Por exemplo, o caminho de instalação padrão para este exemplo é C: Arquivos de \\ \\ Programas Microsoft SDKs \\ Windows \\ v7.0 \\ \\ Exemplos multimídia \\ WindowsAnimation \\ AppDriven.

2.  Execute o seguinte comando: **msbuild AppDriven.sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra Windows Explorer e navegue até o diretório do projeto AppDriven.

2.  Clique duas vezes no ícone do arquivo AppDriven.sln para abrir o projeto Visual Studio.

    > [!Note]  
    > A extensão de nome de arquivo .sln não é mostrada nas configurações de pasta padrão. Nessa situação, ele pode ser identificado por seu ícone exclusivo ou por sua descrição de tipo, "Microsoft Visual Studio Solução".

     

3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável usando o prompt de comando ou Windows Explorer.

2.  Execute **AppDriven.exe** no prompt de comando ou clique duas vezes no ícone para AppDriven.exe no Windows Explorer.

3.  Clique em qualquer lugar na área do cliente e a cor da tela de fundo da janela será mudada para uma cor aleatória.

 

 




