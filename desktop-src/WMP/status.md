---
title: Status (SDK do Windows Media Player)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Aparências móveis do Windows Media Player, exibição de status
- aparências, exibição de status
- referência para capas, exibição de status
- exibição de status em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008689"
---
# <a name="status-windows-media-player-sdk"></a>Status (SDK do Windows Media Player)

Talvez você queira usar uma exibição de status em sua capa. Nesse caso, o elemento status deve ser definido no arquivo de definição de capa. Como alternativa, você também pode exibir essas informações usando o atributo status no elemento Text.

A seção de status do arquivo de definição de capa começa com esta linha:


```C++
[ Status ]

```



Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre a exibição de status em sua capa.


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



Você pode usar o modelo a seguir para a seção de status do arquivo de definição de capa:


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



Você deve usar a ordem mostrada no modelo anterior para informações de exibição de status para cada linha na seção de status. Cada parte da linha é necessária. As seções a seguir descrevem cada item:

-   [Item de status](status-item.md)
-   [Local do status](status-location.md)
-   [Alinhamento de status](status-alignment.md)
-   [Fonte de status](status-font.md)
-   [Cor do status](status-color.md)

Para obter um exemplo de código de status, consulte a [seção status de exemplo](sample-status-section.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




