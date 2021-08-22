---
title: IAgentCharacter setdescritivo
description: IAgentCharacter setdescritivo
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d96765d3faddafef00a28826ec5a9fdd92acb6884ac3aa659ad88ba2c091a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609816"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter:: SetDescription

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




