---
title: Exemplo de interpolador personalizado
description: Mostra como usar a animação do Windows com seu próprio interpolador personalizado, com Direct2D usado para renderização.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104084420"
---
# <a name="custom-interpolator-sample"></a>Exemplo de interpolador personalizado

Mostra como usar a animação do Windows com seu próprio interpolador personalizado, com Direct2D usado para renderização. As imagens de exemplo são carregadas da biblioteca de imagens.

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

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto CustomInterpolator. Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ CustomInterpolator

2.  Execute o seguinte comando: **MSBuild CustomInterpolator. sln**

**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**

1.  Abra o Windows Explorer e navegue até o diretório do projeto CustomInterpolator.

    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".

     

2.  Clique duas vezes no ícone do arquivo CustomInterpolator. sln para abrir o projeto no Visual Studio.

3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.

2.  Execute **CustomInterpolator.exe** no prompt de comando ou clique duas vezes no ícone para CustomInterpolator.exe no Windows Explorer.
3.  Redimensione a janela ou pressione a barra de espaços e as imagens serão organizadas aleatoriamente no meio da área do cliente.

4.  Pressione a seta para cima ou para baixo e as imagens serão aceleradas em direção à parte superior ou inferior da área do cliente.

 

 




