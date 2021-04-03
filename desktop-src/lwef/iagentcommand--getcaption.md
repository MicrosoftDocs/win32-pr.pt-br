---
title: IAgentCommand getCaption
description: IAgentCommand getCaption
ms.assetid: e333faca-e2c2-478a-a803-cbc401793e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44540ba9105e79ba675f8bf78be20e8961f98d0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823678"
---
# <a name="iagentcommandgetcaption"></a>IAgentCommand:: getCaption

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption for Command
);
```

Recupera a [**legenda**](caption-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

O endereço de um BSTR que recebe o valor do texto de [**legenda**](caption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: sethabilitated**](iagentcommand--setenabled.md), [**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 