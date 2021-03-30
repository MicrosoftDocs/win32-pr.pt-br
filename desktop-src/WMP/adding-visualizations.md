---
title: Adicionando visualizações
description: Adicionando visualizações
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Criando capas, visualizações
- Capas do Windows Media Player, visualizações
- capas, visualizações
- visualizações, capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635997"
---
# <a name="adding-visualizations"></a>Adicionando visualizações

Você pode adicionar uma janela de visualização da mesma maneira que adicionou uma janela de vídeo. A mesma capa pode ser usada, mas um elemento **Effects** é usado.

Primeiro, você deve adicionar o elemento **Effects** e dar a ele uma ID e um tamanho:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



Em seguida, você pode atribuir os dois botões uma cadeia de caracteres de código de visualização anterior e seguinte:


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



As camadas e os bitmaps eram os mesmos usados no exemplo de vídeo, exceto que a seta de reprodução foi copiada e invertida horizontalmente.

Por fim, um elemento **Player** simples com o atributo **URL** foi adicionado para escolher uma música a ser reproduzida.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



Você pode ver uma aparência de visualização de trabalho semelhante na seção de exemplo do SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de criação de capa**](skin-creation-guide.md)
</dt> </dl>

 

 




