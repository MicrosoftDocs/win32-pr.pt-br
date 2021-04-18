---
title: IAgentCommands getCaption
description: IAgentCommands getCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105788915"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands:: getCaption

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Recupera a [**legenda**](caption-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

O endereço de um BSTR que recebe o valor da configuração de texto de [**legenda**](caption-property.md) exibida para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands:: getvisível**](iagentcommands--getvisible.md), [**IAgentCommands:: getvoice**](iagentcommands--getvoice.md)


 

 