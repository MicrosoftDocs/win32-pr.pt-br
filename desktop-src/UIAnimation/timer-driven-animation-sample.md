---
title: Timer-Driven de animação
description: Mostra como usar a animação Windows animação com o temporizador de animação, enquanto usa GDI+ para animar a cor da tela de fundo de uma janela.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8071d51906ba2d0d7b59acb7b1b5531fcb5c577fbbf0d47ab5039d3f43e2eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008156"
---
# <a name="timer-driven-animation-sample"></a>Timer-Driven de animação

Mostra como usar a animação Windows animação com o temporizador de animação, enquanto usa GDI+ para animar a cor da tela de fundo de uma janela.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Localização                               | Caminho/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galeria de código                           | [Windows Código de exemplo do Gerenciador de Animação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação. Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para Windows 7, os exemplos serão instalados em C: Arquivos de Programas \\ \\ SDKs da Microsoft Windows \\ \\ exemplos v7.0. \\

## <a name="building-the-sample"></a>Compilando o exemplo

Use um dos métodos a seguir para criar o exemplo.

**Para criar o exemplo no prompt de comando**

1.  Abra a janela Prompt de Comando e navegue até o diretório do projeto TimerDriven. Por exemplo, o caminho de instalação padrão para este exemplo é C: Arquivos de \\ \\ Programas Microsoft SDKs \\ Windows \\ v7.0 \\ \\ Amostras De multimídia \\ WindowsAnimation \\ TimerDriven.

2.  Execute o seguinte comando: **msbuild TimerDriven.sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra Windows Explorer e navegue até o diretório do projeto TimerDriven.

2.  Clique duas vezes no ícone do arquivo TimerDriven.sln para abrir o projeto Visual Studio.

    > [!Note]  
    > A extensão de nome de arquivo .sln não é mostrada nas configurações de pasta padrão. Nessa situação, ele pode ser identificado por seu ícone exclusivo ou por sua descrição de tipo, "Microsoft Visual Studio Solução".

     

3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável usando o prompt de comando ou Windows Explorer.

2.  Execute **TimerDriven.exe** no prompt de comando ou clique duas vezes no ícone para TimerDriven.exe no Windows Explorer.

3.  Clique em qualquer lugar na área do cliente e a cor da tela de fundo da janela será mudada para uma cor aleatória.

 

 




