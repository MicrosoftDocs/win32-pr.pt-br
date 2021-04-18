---
description: A maioria dos aplicativos tenta dar suporte a WYSIWYG (o que você vê é o que você obtém).
ms.assetid: 34a1f37c-0fbf-451b-bb55-80ad85bcd4de
title: Exibição e saída WYSIWYG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c03e4fa653c0d8e891cb079a7a7e7a003f9ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791586"
---
# <a name="wysiwyg-display-and-output"></a>Exibição e saída WYSIWYG

A maioria dos aplicativos tenta dar suporte a WYSIWYG (o que você vê é o que você obtém). Isso significa que o texto desenhado com uma fonte Helvetica negrito de 10 pontos na janela do aplicativo deve ter uma aparência semelhante quando é impresso. A obtenção de uma saída WYSIWYG verdadeira é praticamente impossível e mesmo indesejável na maioria dos casos. Isso é devido, em parte, às diferenças nas tecnologias de vídeo e impressora; um pixel em uma tela geralmente é maior do que um ponto em uma impressora laser comum. A exibição de distâncias também é diferente; um usuário de computador normalmente fica com cerca de dois pés de distância da tela, mas os olhos de um leitor são, em geral, um pé ou menos da página impressa.

Para compensar as diferenças de legibilidade entre as telas e a página impressa, o sistema dá suporte a uma unidade chamada de polegada lógica que é sempre especificada em pixels. Para uma exibição de vídeo, a polegada lógica é sempre maior que a polegada física para compensar a distância de exibição mais longa e a resolução mais espessa (geralmente). Para impressoras, a polegada lógica é sempre igual à polegada física.

Para obter um efeito WYSIWYG ao desenhar texto, dois problemas relacionados estão envolvidos: fazer com que caracteres individuais pareçam os mesmos e o layout de página independente de dispositivo. Para resolver o primeiro problema, um aplicativo pode usar a função [**CreateFont**](/windows/desktop/api/wingdi/nf-wingdi-createfonta) para especificar o nome da fonte e o tamanho de uma fonte ideal (ou lógica) e, em seguida, chamar a função [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para identificar o contexto do dispositivo de exibição ou de impressora. Quando o aplicativo chama **SelectObject** , o sistema seleciona uma fonte física que é a correspondência mais próxima possível à fonte lógica especificada. Quando o sistema seleciona a fonte de vídeo, ele escolhe uma fonte física maior do que o tamanho real. Isso ocorre devido à maior polegada lógica na exibição. No entanto, da perspectiva do usuário, ele parece estar muito próximo da altura correta. Quando o sistema seleciona a fonte da impressora, ele escolhe uma fonte física que é, na verdade, o tamanho solicitado. Para obter mais informações sobre fontes e saída de texto, consulte [fontes e texto](/windows/desktop/gdi/fonts-and-text).

O segundo problema, que é o layout de página independente de dispositivo, pode ser resolvido pelo uso de métricas TrueType. Isso é verdadeiro mesmo ao manter a compatibilidade com versões de 16 bits do Windows. Para obter mais informações, consulte [usando métricas TrueType portáteis](/windows/desktop/gdi/using-portable-truetype-metrics).

Para obter um efeito WYSIWYG ao desenhar gráficos de bitmap, um aplicativo pode recuperar a largura e a altura, em polegadas lógicas, da tela e da página impressa. Usando esses valores, o aplicativo pode criar fatores de dimensionamento horizontais e verticais para manter a proporção de imagens de bitmap quando elas são desenhadas em uma impressora. Para obter mais informações sobre bitmaps e saída de bitmap, consulte [bitmaps](/windows/desktop/gdi/bitmaps).

 

 
