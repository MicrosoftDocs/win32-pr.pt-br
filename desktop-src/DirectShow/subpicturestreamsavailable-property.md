---
description: A propriedade SubpictureStreamsAvailable recupera o número de fluxos de subimagem disponíveis no título atual.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propriedade SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758827"
---
# <a name="subpicturestreamsavailable-property"></a>Propriedade SubpictureStreamsAvailable

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `SubpictureStreamsAvailable` propriedade recupera o número de fluxos de subimagem disponíveis no título atual.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Valor Retornado

Retorna o número de fluxos disponíveis como um inteiro.

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. Para consultar cada fluxo para seu atributo de idioma, primeiro chame esse método para obter o limite superior.

A numeração de fluxo é baseada em zero.

 

 



