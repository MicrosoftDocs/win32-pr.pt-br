---
title: Começar com TEMA e EXIBIÇÃO
description: Começar com TEMA e EXIBIÇÃO
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- criando capas, elemento THEME
- Windows Media Player capas, elemento THEME
- skins, elemento THEME
- arquivos de definição de capa, elemento THEME
- Elemento THEME
- criando capas, elemento VIEW
- Windows Media Player capas, elemento VIEW
- skins, elemento VIEW
- arquivos de definição de capa, elemento VIEW
- Elemento VIEW
- elementos, VIEW
- elementos, THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bcb18a9d56a8780e56d81d6de60ca269036c72
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883715"
---
# <a name="start-with-theme-and-view"></a>Começar com TEMA e EXIBIÇÃO

Cada capa deve ter exatamente um **elemento THEME** e pelo menos um **elemento VIEW.**

Usando seu editor de texto, crie o seguinte texto:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



Deixe algumas linhas em branco antes da marca **VIEW** de fechamento, pois você adicionará mais código aqui mais tarde.

Salve o arquivo com qualquer nome de arquivo que desejar, mas certifique-se de que a extensão seja .wms. Por exemplo, um nome de arquivo típico pode ser skinone.wms.

Cada capa deve começar com &lt; THEME e terminar com &gt; </THEME> . Você só pode ter **um elemento THEME** em sua capa, mas deve ter um.

Você também deve ter pelo menos um **elemento VIEW.** Você pode ter mais de um **VIEW**, mas este exemplo tem apenas um. Você deve ter um &lt; VIEW de abertura e um VIEW de &gt; &lt; &gt; fechamento. Observe que a marca /VIEW de abertura não fecha a marca imediatamente, mas inclui vários atributos antes do colchete angular de &lt; &gt; fechamento (>). Os seguintes atributos são usados no **elemento THEME** neste exemplo:

**clippingColor**

Você nem sempre precisará do **atributo clippingColor** se as bordas da sua capa são retangulares. A capa neste exemplo é em forma de oval, portanto, você precisa de uma cor de recorte para as partes da capa pelas quais você deseja ver a área de trabalho; essencialmente todas as partes fora da oval. Nesta capa de exemplo, vamos usar um amarelo escuro, especificado como " \# CCCC00" no formato Web. Os motivos para essa escolha são determinados em [Criando o arquivo de arte primário.](creating-the-primary-art-file.md) Essencialmente, esse valor sempre será um número que você obterá do seu programa de arte.

**backgroundImage**

Esse é o nome do arquivo de arte principal. Ele deve ser o nome e o caminho exatos do arquivo de arte principal. Há suporte apenas para arquivos BMP, JPG, GIF e PNG, e o BMP é recomendado.

**Titlebar**

Essa capa não tem uma **titleBar,** portanto, o valor será "false". Você só deseja uma barra de título se quiser que sua capa tenha uma cor da tela de fundo e seja retangular.

Certifique-se de colocar o colchete angular de fechamento (>) após o valor **titleBar** para indicar que você concluiu a definição de **VIEW**. Deixe algumas linhas em branco antes das marcas **VIEW** e **THEME de** fechamento. Você precisará das linhas para o código que adicionará posteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




