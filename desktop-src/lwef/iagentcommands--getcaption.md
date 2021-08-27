---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6eb40b0be58695e79a02ab0ad67ad0d26a47bd13a1637dc1d1f5a4380a7429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749876"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands::GetCaption

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Recupera a [**legenda de uma**](caption-property.md) coleção de [**Comandos.**](/windows/desktop/lwef/the-commands-collection-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

O endereço de um BSTR que recebe o valor da [**configuração**](caption-property.md) de texto Legenda exibida para uma coleção [**comandos.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)


 

 