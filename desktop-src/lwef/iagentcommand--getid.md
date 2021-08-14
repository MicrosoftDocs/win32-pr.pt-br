---
title: IAgentCommand GetID
description: IAgentCommand GetID
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbe051ab91a389c7a1a0d0ee6a445a9d2eb6107ea7f6a2755daa1a0bb0215f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477641"
---
# <a name="iagentcommandgetid"></a>IAgentCommand:: GetID

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

Recupera a ID de um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

O endereço de uma variável que recebe a ID de um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)


 

 