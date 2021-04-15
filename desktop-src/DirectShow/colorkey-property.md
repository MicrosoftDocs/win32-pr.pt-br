---
description: A propriedade ColorKey define ou recupera a chave de cor usada em legendas ocultas.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propriedade ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456489"
---
# <a name="colorkey-property"></a>Propriedade ColorKey

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `ColorKey` propriedade define ou recupera a chave de cor usada em Legendagem oculta.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa a cor a ser usada como um plano de fundo transparente para texto com legenda codificada. O valor padrão em 256 cores é magenta e off-preto em qualquer outra intensidade de cor.

## <a name="remarks"></a>Comentários

Esta propriedade é de leitura/gravação. Essa propriedade só se aplica a legendas fechadas, se existir, não ao fluxo de subimagem.

 

 



