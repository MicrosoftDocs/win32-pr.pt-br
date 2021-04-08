---
description: O método Stop interrompe a reprodução.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Método Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922377"
---
# <a name="stop-method-directshow"></a>Método Stop (DirectShow)

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `Stop` método para a reprodução.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se [**EnableResetOnStop**](enableresetonstop-property.md) for definido como true, `Stop` a chamada colocará o navegador de DVD, junto com o restante do grafo de filtro, em um estado parado, o que significa que, na próxima vez que o usuário pressionar o botão **reproduzir** , a reprodução será iniciada no início do disco. Se **EnableResetOnStop** for definido como true, a reprodução será retomada de onde parou quando o usuário emitir o comando Next **Play** .

 

 



