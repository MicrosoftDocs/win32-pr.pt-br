---
description: A propriedade FullScreenmode define ou recupera um valor que indica se a exibição está no modo de tela inteira.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propriedade FullScreenmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087284"
---
# <a name="fullscreenmode-property"></a>Propriedade FullScreenmode

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `FullScreenMode` propriedade define ou recupera um valor que indica se a exibição está no modo de tela inteira.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se a reprodução de tela inteira deve ser habilitada ou desabilitada.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de false.



| Valor | Descrição                                            |
|-------|--------------------------------------------------------|
| true  | Habilite a reprodução em tela inteira. Esse é o valor padrão. |
| false | Desabilite a reprodução em tela inteira.                          |



 

O modo de tela inteira só está disponível quando o controle MSWebDVD está em execução no modo de janela.

 

 



