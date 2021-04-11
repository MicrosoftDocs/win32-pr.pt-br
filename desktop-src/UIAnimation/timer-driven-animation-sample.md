---
title: Exemplo de animação de Timer-Driven
description: Mostra como usar a animação do Windows com o temporizador de animação, ao usar o GDI+ para animar a cor do plano de fundo de uma janela.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104293876"
---
# <a name="timer-driven-animation-sample"></a>Exemplo de animação de Timer-Driven

Mostra como usar a animação do Windows com o temporizador de animação, ao usar o GDI+ para animar a cor do plano de fundo de uma janela.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local                               | Caminho/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Kit de desenvolvimento de software do Microsoft Windows 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galeria de código                           | [Código de exemplo do Gerenciador de animação do Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação. Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para o Windows 7, os exemplos serão instalados em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos.

## <a name="building-the-sample"></a>Compilando o exemplo

Use um dos métodos a seguir para criar o exemplo.

**Para criar o exemplo no prompt de comando**

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto TimerDriven. Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ TimerDriven.

2.  Execute o seguinte comando: **MSBuild TimerDriven. sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra o Windows Explorer e navegue até o diretório do projeto TimerDriven.

2.  Clique duas vezes no ícone do arquivo TimerDriven. sln para abrir o projeto no Visual Studio.

    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".

     

3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.

2.  Execute **TimerDriven.exe** no prompt de comando ou clique duas vezes no ícone para TimerDriven.exe no Windows Explorer.

3.  Clique em qualquer lugar na área do cliente e a cor do plano de fundo da janela será alterada para uma cor aleatória.

 

 




