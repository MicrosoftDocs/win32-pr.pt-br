---
title: texto (SDK do Windows Media Player)
description: Texto
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Aparências móveis, texto
- capas, texto
- referência de capas, texto
- texto em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55027415222516e72df61afab01a14cceb503528467bf329264014c94bf31ed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118094"
---
# <a name="text-windows-media-player-sdk"></a>texto (SDK do Windows Media Player)

Talvez você queira usar uma ou mais caixas de exibição de texto em sua capa. Cada caixa de exibição de texto que você usa deve ser definida no arquivo de definição de capa. Se você não definir uma caixa de exibição de texto nesta seção, sua capa não será capaz de usá-la.

A seção de texto do arquivo de definição de capa começa com esta linha:


```C++
[ Text ]

```



Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das caixas de exibição de texto em sua capa


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



Você pode usar o modelo a seguir para a seção de texto do arquivo de definição de capa:


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



Você deve usar a ordem mostrada no modelo anterior para informações da caixa de exibição de texto para cada linha na seção de texto. Cada parte da linha é necessária. As seções a seguir descrevem cada item em detalhes.

1.  [Tipo de texto](text-type.md)
2.  [Local do texto](text-location.md)
3.  [Alinhamento de texto](text-alignment.md)
4.  [Fonte do texto](text-font.md)
5.  [Cor do texto](text-color.md)

Para obter um exemplo de código de texto, consulte a [seção texto de exemplo](sample-text-section.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




