---
title: Exemplo de animação de Application-Driven
description: Mostra a animação do Windows na configuração controlada por aplicativo usando Direct2D para animar a cor do plano de fundo de uma janela e sincronizar com a taxa de atualização.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "105810423"
---
# <a name="application-driven-animation-sample"></a>Exemplo de animação de Application-Driven

Mostra a animação do Windows na configuração controlada por aplicativo usando Direct2D para animar a cor do plano de fundo de uma janela e sincronizar com a taxa de atualização.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local                               | Caminho/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Kit de desenvolvimento de software do Microsoft Windows 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galeria de código                           | [Código de exemplo do Gerenciador de animação do Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação. Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para o Windows 7, os exemplos serão instalados em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos.

## <a name="building-the-sample"></a>Compilando o exemplo

Use um dos métodos a seguir para criar o exemplo.

**Para criar o exemplo no prompt de comando**

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto AppDriven. Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ AppDriven.

2.  Execute o seguinte comando: **MSBuild AppDriven. sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra o Windows Explorer e navegue até o diretório do projeto AppDriven.

2.  Clique duas vezes no ícone do arquivo AppDriven. sln para abrir o projeto no Visual Studio.

    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".

     

3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.

2.  Execute **AppDriven.exe** no prompt de comando ou clique duas vezes no ícone para AppDriven.exe no Windows Explorer.

3.  Clique em qualquer lugar na área do cliente e a cor do plano de fundo da janela será alterada para uma cor aleatória.

 

 




