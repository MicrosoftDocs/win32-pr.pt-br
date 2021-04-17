---
description: O método StillOff retoma a reprodução, cancelando o modo ainda.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Método StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780040"
---
# <a name="stilloff-method"></a>Método StillOff

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `StillOff` método retoma a reprodução, cancelando o modo ainda.

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O [navegador de DVD](dvd-navigator-filter.md) entra em modo ainda quando encontra um quadro ainda criado no disco. Ele notifica seu aplicativo enviando um \_ evento do EC DVD \_ ainda \_ . O modo ainda é diferente do DVD Navigator estar em um estado pausado devido a uma operação de usuário. Chamar `StillOff` retoma a reprodução a partir do modo ainda, mas não reinicia o navegador de DVD quando ele está em um estado de pausa.

 

 



