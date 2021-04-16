---
description: A propriedade subpictureize define ou recupera o estado atual da subimagem (ativado ou desativado).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Propriedade subpictureize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787130"
---
# <a name="subpictureon-property"></a>Propriedade subpictureize

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `SubpictureOn` propriedade define ou recupera o estado da subimagem atual (ativado ou desativado).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se a subimagem é exibida.

## <a name="remarks"></a>Comentários

Essa propriedade não afeta a exibição de legendas ocultas. As legendas ocultas são inseridas no fluxo de vídeo. As subimagems de DVD são transportadas em um fluxo separado.

Quando o fluxo de subimagem é alterado usando [**CurrentSubpictureStream**](currentsubpicturestream-property.md), a `SubpictureOn` Propriedade alterna para **verdadeiro**.

Essa propriedade é de leitura/gravação com um valor padrão de false.

 

 



