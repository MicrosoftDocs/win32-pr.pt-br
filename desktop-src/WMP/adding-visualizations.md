---
title: Adicionando visualizações
description: Adicionando visualizações
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Criando capas, visualizações
- Windows Media Player capas, visualizações
- capas, visualizações
- visualizações, capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d236990d3e29cf4e51dbb46e8e1269b0c8a50ccaf205940a6f34b97c89fa6e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619146"
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

 

 




