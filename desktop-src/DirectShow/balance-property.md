---
description: A propriedade Balance define ou recupera o saldo do locutor para a saída do fluxo de áudio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Propriedade Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4faa8bcacb8c4603dcb67ee6cc617ced4b31bd7afa3afa16d3ba3831040a004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689376"
---
# <a name="balance-property"></a>Propriedade Balance

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `Balance` propriedade define ou recupera o saldo do locutor para a saída do fluxo de áudio.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa os níveis de saldo. O intervalo de entrada acessível é de -10.000 a 10.000. Um valor de 0 define um saldo neutro, que são os alto-falantes esquerdo e direito, que recebe o mesmo sinal de áudio de amplitude.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de 0, o que significa que ambos os alto-falantes recebem sinais de áudio equivalentes. Assim como acontece com [**a propriedade Volume,**](volume-property.md) as unidades correspondem a decibéis .01 (multiplicados por -1 quando


```
iBalance
```



é um valor positivo). Por exemplo, um valor de 1000 indica 10 dB no canal direito e 90 dB no canal esquerdo.

 

 



