---
title: Exemplo de comparação de prioridade
description: Mostra como usar a animação Windows com sua própria Comparação de Prioridade, usando Direct2D para renderização.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafeb2332de02115cbb8af2f2afd69a2fc783be9908a91dbb4e9bb0615876bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008186"
---
# <a name="priority-comparison-sample"></a>Exemplo de comparação de prioridade

Mostra como usar a animação Windows com sua própria Comparação de Prioridade, usando Direct2D para renderização.

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

1.  Abra a janela Prompt de Comando e navegue até o diretório do projeto PriorityComparison. Por exemplo, o caminho de instalação padrão para este exemplo é C: Arquivos de Programas \\ \\ Microsoft SDKs \\ Windows \\ v7.0 \\ \\ Samples Multimídia \\ WindowsAnimation \\ PriorityComparison.

2.  Execute o seguinte comando: **msbuild PriorityComparison.sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra Windows Explorer e navegue até o diretório do projeto PriorityComparison.

2.  Clique duas vezes no ícone do arquivo PriorityComparison.sln para abrir o projeto Visual Studio.

    > [!Note]  
    > A extensão de nome de arquivo .sln não é mostrada nas configurações de pasta padrão. Nessa situação, ele pode ser identificado por seu ícone exclusivo ou por sua descrição de tipo, "Microsoft Visual Studio Solução".

     

3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável usando o prompt de comando ou Windows Explorer.

2.  Execute **PriorityComparison.exe** no prompt de comando ou clique duas vezes no ícone para PriorityComparison.exe no Windows Explorer.

3.  As imagens de exemplo são carregadas da Biblioteca de Imagens. Reesize a janela ou pressione a barra de espaços e as imagens serão movedas para o centro.

4.  Use as teclas de seta para a esquerda e para a direita para selecionar imagens diferentes (quanto mais rápida a tecla for pressionada, mais rápido a seleção será mudada).

5.  Use as teclas de seta para cima e para baixo para criar uma onda pelas imagens (quanto mais rápida a tecla for pressionada, mais rápida será a onda).

 

 




