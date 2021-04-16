---
title: Seção de letreiro de exemplo
description: Seção de letreiro de exemplo
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Aparências móveis do Windows Media Player, letreiros
- capas, letreiros
- referência para capas, letreiros
- letreiros em capas, seção Marquee
- arquivos de definição de capa, seção de letreiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453686"
---
# <a name="sample-marquee-section"></a>Seção de letreiro de exemplo

As linhas a seguir mostram uma seção de letreiro típica de um arquivo de definição de capa:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Isso define uma caixa de exibição de letreiro que mostra o título e o autor se ambos estiverem definidos, o título se apenas título for definido ou o nome do autor se apenas autor for definido. Se nenhum for definido, nada será exibido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Marquee**](marquee.md)
</dt> </dl>

 

 




