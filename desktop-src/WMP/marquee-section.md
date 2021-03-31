---
title: Seção de letreiro
description: Seção de letreiro
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Aparências móveis do Windows Media Player, letreiros
- capas, letreiros
- Criando capas, seção Marquee
- escrevendo código para capas, seção Marquee
- letreiros em capas, seção Marquee
- arquivos de definição de capa, seção de letreiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637241"
---
# <a name="marquee-section"></a>Seção de letreiro

A seção Marquee contém informações sobre a caixa de texto Marquee, que exibirá o texto de rolagem:


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



Isso exibirá o título e o autor do item de mídia atual, embora você possa exibir qualquer tipo de texto no letreiro. Por exemplo, você também pode incluir nome de arquivo, status e lista de reprodução em seu letreiro.

> [!Note]  
> Para manter a compatibilidade com versões do Windows Media Player Mobile anteriores ao Windows Media Player 10 Mobile, o uso de "Marquis" em um arquivo de definição de capa ainda é considerado válido.

 

Para obter mais informações sobre a seção Marquee, consulte [letreiro](marquee.md) na referência de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo o código**](writing-the-code.md)
</dt> </dl>

 

 




