---
description: A propriedade SubpictureOn define ou recupera o estado atual da subpicture (on ou off).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Propriedade SubpictureOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692df6b69bc960562e9acd223a0e4e156fe00de2206146f609ba15d550b7a961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951765"
---
# <a name="subpictureon-property"></a>Propriedade SubpictureOn

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `SubpictureOn` propriedade define ou recupera o estado atual da subpicture (on ou off).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliana que indica se a subpicture é exibida.

## <a name="remarks"></a>Comentários

Essa propriedade não afeta a exibição de Legendas Fechadas. Legendas fechadas são inseridas no fluxo de vídeo. Subtípicos de DVD são transportados em um fluxo separado.

Quando o fluxo de subpicture é alterado [**usando CurrentSubpictureStream**](currentsubpicturestream-property.md), a `SubpictureOn` propriedade alterna para **True.**

Essa propriedade é de leitura/gravação com um valor padrão de false.

 

 



