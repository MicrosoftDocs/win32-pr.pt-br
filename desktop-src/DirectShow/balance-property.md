---
description: A propriedade Balance define ou recupera o equilíbrio do alto-falante para a saída do fluxo de áudio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Propriedade Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760288"
---
# <a name="balance-property"></a>Propriedade Balance

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `Balance` propriedade define ou recupera o equilíbrio do alto-falante para a saída do fluxo de áudio.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa os níveis de saldo. O intervalo de entrada permitido é de-10.000 a 10.000. Um valor de 0 define um equilíbrio neutro, que é o mesmo que os alto-falantes esquerdo e direito recebem o mesmo sinal de áudio de amplitude.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de 0, o que significa que ambos os alto-falantes recebem sinais de áudio equivalentes. Assim como acontece com a propriedade [**volume**](volume-property.md) , as unidades correspondem a 0,01 decibéis (multiplicado por-1 quando


```
iBalance
```



é um valor positivo). Por exemplo, um valor de 1000 indica 10 dB no canal direito e 90 dB no canal à esquerda.

 

 



