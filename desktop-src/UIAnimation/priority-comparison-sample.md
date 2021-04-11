---
title: Exemplo de comparação de prioridade
description: Mostra como usar a animação do Windows com sua própria comparação de prioridade, usando Direct2D para renderização.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104084419"
---
# <a name="priority-comparison-sample"></a>Exemplo de comparação de prioridade

Mostra como usar a animação do Windows com sua própria comparação de prioridade, usando Direct2D para renderização.

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

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto PriorityComparison. Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ PriorityComparison.

2.  Execute o seguinte comando: **MSBuild PriorityComparison. sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra o Windows Explorer e navegue até o diretório do projeto PriorityComparison.

2.  Clique duas vezes no ícone do arquivo PriorityComparison. sln para abrir o projeto no Visual Studio.

    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".

     

3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.

2.  Execute **PriorityComparison.exe** no prompt de comando ou clique duas vezes no ícone para PriorityComparison.exe no Windows Explorer.

3.  As imagens de exemplo são carregadas da biblioteca de imagens. Redimensione a janela ou pressione a barra de espaços e as imagens serão movidas para o centro.

4.  Use as teclas de seta para a esquerda e para a direita para selecionar imagens diferentes (quanto mais rápida a chave for pressionada, mais rapidamente a seleção será alterada).

5.  Use as teclas de seta para cima e para baixo para criar uma onda por meio das imagens (quanto mais rápida for pressionada, mais rápida será a onda).

 

 




