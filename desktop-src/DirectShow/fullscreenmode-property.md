---
description: A propriedade FullScreenmode define ou recupera um valor que indica se a exibição está no modo de tela inteira.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propriedade FullScreenmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 103938afa6710b858329147eafadec4e06fd7d2ba244b896dd1ac39c74cd12c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015614"
---
# <a name="fullscreenmode-property"></a>Propriedade FullScreenmode

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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

 

 



