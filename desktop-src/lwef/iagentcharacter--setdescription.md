---
title: IAgentCharacter setdescritivo
description: IAgentCharacter setdescritivo
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364497"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter:: SetDescription

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Define a descrição do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

Um BSTR que define a descrição para o caractere. A descrição padrão de um caractere é definida quando é compilada com o editor de caracteres do Microsoft Agent. A configuração descrição é opcional e pode não ser fornecida para todos os caracteres. Você pode alterar a descrição do caractere usando **IAgentCharacter:: SetDescription**; no entanto, esse valor não é persistente (armazenado permanentemente). A descrição do caractere é revertida para sua configuração padrão sempre que o caractere é carregado pela primeira vez por um cliente.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: GetDescription**](iagentcharacter--getdescription.md)


 

 




