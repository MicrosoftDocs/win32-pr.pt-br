---
title: Seção De marca de exemplo
description: Seção De marca de exemplo
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player Capas móveis, marques
- skins,marquees
- referência para capas, marquees
- marques em capas, seção Marquee
- arquivos de definição de capa, seção Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f8a3e013bb3a09a06f03715f0e7c4914e8e8d344c55843a643d5b8a9bf0479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508116"
---
# <a name="sample-marquee-section"></a>Seção De marca de exemplo

As linhas a seguir mostram uma seção típica do Marquee de um arquivo de definição de capa:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Isso define uma caixa de exibição de letreiro que mostra o título e o autor se ambos estão definidos, o título se apenas Title estiver definido ou o nome do autor, se apenas Autor estiver definido. Se nenhum deles estiver definido, nada será exibido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Marquee**](marquee.md)
</dt> </dl>

 

 




