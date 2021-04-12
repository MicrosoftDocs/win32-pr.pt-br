---
title: IAgentCommand getabilited
description: IAgentCommand getabilited
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454018"
---
# <a name="iagentcommandgetenabled"></a>IAgentCommand:: getabilited

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

Recupera o valor da propriedade [**Enabled**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

O endereço de uma variável que recebe **true** se o [**comando**](/windows/desktop/lwef/the-command-object) estiver habilitado ou **false** se estiver desabilitado. Um **comando** desabilitado não pode ser selecionado.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setvisível**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 