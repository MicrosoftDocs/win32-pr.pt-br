---
title: Iniciar com tema e exibição
description: Iniciar com tema e exibição
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- Criando capas, elemento THEME
- Capas do Windows Media Player, elemento THEME
- capas, elemento THEME
- arquivos de definição de capa, elemento THEME
- Elemento THEME
- Criando capas, elemento VIEW
- Capas do Windows Media Player, elemento VIEW
- aparência, elemento VIEW
- arquivos de definição de capa, elemento VIEW
- Elemento VIEW
- elementos, exibição
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822973"
---
# <a name="start-with-theme-and-view"></a>Iniciar com tema e exibição

Cada capa deve ter exatamente um elemento **Theme** e pelo menos um elemento **View** .

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



Deixe algumas linhas em branco antes da marca de **exibição** de fechamento, pois você adicionará mais código aqui mais tarde.

Salve o arquivo com qualquer nome de arquivo que desejar, mas certifique-se de que a extensão seja. WMS. Por exemplo, um nome de arquivo típico pode ser skinone. WMS.

Cada capa deve começar com <THEME> e terminar com </THEME>. Você só pode ter um elemento **Theme** em sua capa, mas deve ter um.

Você também deve ter pelo menos um elemento de **exibição** . Você pode ter mais de uma **exibição**, mas este exemplo tem apenas uma. Você deve ter uma abertura <VIEW> e um fechamento <VIEW>. Observe que a marca de abertura </VIEW> não fecha a marca imediatamente, mas inclui vários atributos antes do colchete angular de fechamento (>). Os seguintes atributos são usados no elemento **Theme** neste exemplo:

**clippingColor**

Nem sempre será necessário o atributo **clippingColor** se as bordas da sua capa forem retangulares. A capa neste exemplo é formada por oval, portanto, você precisa de uma cor de recorte para as partes da capa para as quais você deseja ver a área de trabalho; essencialmente, todas as partes fora da oval. Nesta capa de exemplo, usaremos um amarelo escuro, especificado como " \# CCCC00" no formato da Web. Os motivos para essa escolha são fornecidos na [criação do arquivo de arte principal](creating-the-primary-art-file.md). Essencialmente, esse valor sempre será um número que você obtém do seu programa de arte.

**backgroundImage**

Esse é o nome do arquivo de arte primário. Deve ser o nome exato do arquivo e o caminho do seu arquivo de arte primário. Somente arquivos BMP, JPG, GIF e PNG têm suporte e o BMP é recomendado.

**titleBar**

Essa capa não tem uma **TitleBar**, portanto, o valor será "false". Você só desejará uma barra de título se quiser que sua capa tenha uma cor de plano de fundo e seja retangular.

Certifique-se de colocar o colchete angular de fechamento (>) após o valor da **TitleBar** para indicar que você terminou de definir a **exibição**. Deixe algumas linhas em branco antes da **exibição** de fechamento e das marcas de **tema** . Você precisará das linhas para o código que será adicionado posteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




