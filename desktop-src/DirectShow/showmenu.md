---
description: O evento ShowMenu é enviado quando o disco habilita ou desabilita a exibição de um menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56eb6767a8144bab3de832570db63bc4e2cdc012490f776f52b6c8977cce9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050446"
---
# <a name="showmenu"></a>ShowMenu

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

Especifica qual menu foi habilitado ou desabilitado como um valor Number.



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

Especifica se a operação está habilitada ou desabilitada como booliana.

</dd> </dl>

 

 



