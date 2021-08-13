---
title: IAgentCommand getVisible
description: IAgentCommand getVisible
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d25636b326c32b67d868d145e32e3f1fc17ef3e1fc1c515e288927e5497a9fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477631"
---
# <a name="iagentcommandgetvisible"></a>IAgentCommand:: getVisible

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

Recupera o valor da propriedade [**Visible**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

O endereço de uma variável que recebe a propriedade [**Visible**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: setvisível**](iagentcommand--setvisible.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 