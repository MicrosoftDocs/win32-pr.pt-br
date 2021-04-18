---
description: A propriedade DisableAutoMouseProcessing habilita ou desabilita a funcionalidade de processamento de mouse do objeto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Propriedade DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456409"
---
# <a name="disableautomouseprocessing-property"></a>Propriedade DisableAutoMouseProcessing

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DisableAutoMouseProcessing` Propriedade habilita ou desabilita a funcionalidade de processamento de mouse do objeto **MSWebDVD** .

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se o processamento padrão do mouse deve ser desabilitado.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de false. O objeto **MSWebDVD** manipula automaticamente ações do mouse para menus na tela de DVD por padrão; os usuários podem realçar e ativar botões de menu sem programação especial pelo aplicativo. Um aplicativo pode desativar essa funcionalidade padrão de manipulação de mouse definindo essa propriedade como **true**. Quando o processamento automático do mouse é desativado, um aplicativo deve usar os vários métodos e propriedades relacionados ao botão para manipular as movimentações do mouse e os cliques do mouse nos menus na tela. Além disso, um aplicativo pode usar os métodos relacionados ao botão para substituir a manipulação automática do mouse, mesmo quando `DisableAutoMouseProcessing` é definido como **false**.

 

 



