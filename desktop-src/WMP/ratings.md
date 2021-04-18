---
title: Classificações
description: Classificações
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Aparências móveis do Windows Media Player, classificações
- capas, classificações
- referência para capas, classificações
- classificações em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791575"
---
# <a name="ratings"></a>Classificações

Ao criar uma capa para o Windows Media Player 10,1 Mobile, você pode exibir a classificação associada ao conteúdo baseado em áudio do Windows Media que está sendo executado no momento. A classificação é exibida como uma estrela com um número. A estrela será numerada uma a cinco, denotando a classificação atual desse conteúdo. Se o conteúdo não for classificado, a estrela será numerada como zero.

A seção ratings do arquivo de definição de capa começa com esta linha:


```C++
[ Ratings ]

```



Em seguida, você deve adicionar uma linha que contém informações sobre o tamanho e o local do ícone de classificações em sua capa.


```C++
147, 3, 22, 21       ratings96S.gif

```



Você pode usar o modelo a seguir para a seção de classificações do arquivo de definição de capa:


```C++
// <Location>           <Image>
// ---------------      --------------------
```



Você também pode atribuir um valor de classificações a um item de mídia por meio da interface do usuário no Windows Media Player 10,1 Mobile e, na próxima vez em que o dispositivo for sincronizado com o computador, o novo valor de classificações será propagado para esse item de mídia se ele residir na biblioteca do Windows Media Player 10.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




