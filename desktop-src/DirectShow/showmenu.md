---
description: O evento de menu é enviado quando o disco habilita ou desabilita a exibição de um menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: Menu de tudo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919942"
---
# <a name="showmenu"></a>Menu de tudo

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `ShowMenu` evento é enviado quando o disco habilita ou desabilita a exibição de um menu.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

Especifica qual menu foi habilitado ou desabilitado como um valor numérico.



| Valor | Descrição |
|-------|-------------|
| 2     | Título       |
| 3     | Root        |
| 4     | Subimagem  |
| 5     | Áudio       |
| 6     | Ângulo       |
| 7     | Capítulo     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Especifica se a operação está habilitada ou desabilitada como um booliano.

</dd> </dl>

 

 



