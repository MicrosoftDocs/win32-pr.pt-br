---
description: A propriedade CurrentDomain recupera o domínio de DVD no qual o objeto MSWebDVD está.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Propriedade CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456660"
---
# <a name="currentdomain-property"></a>Propriedade CurrentDomain

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentDomain` propriedade recupera o domínio de DVD no qual o objeto MSWebDVD está.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o domínio atual.

## <a name="remarks"></a>Comentários

Os valores possíveis da propriedade são:



| Valor | Descrição          |
|-------|----------------------|
| 1     | Primeira reprodução           |
| 2     | Menu Gerenciador de vídeo   |
| 3     | Menu de conjunto de título de vídeo |
| 4     | Título                |
| 5     | Stop                 |



 

Chame esse método para garantir que o navegador de DVD esteja em um domínio válido para o método que você está prestes a chamar. Por exemplo, antes de chamar [**PlayTitle**](playtitle-method.md), verifique a propriedade para certificar-se `CurrentDomain` de que o navegador de DVD não está no domínio de parada ou da primeira reprodução.

 

 



