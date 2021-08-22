---
title: IAgentBallike GetFontStrikethru
description: IAgentBallike GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b15bfbc120f7c8d614839f55ec985a3bdbdb3f840e5a07d615f7de0dfc75e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751020"
---
# <a name="iagentballoongetfontstrikethru"></a>IAgentBallike::GetFontStrikethru

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

Indica se a fonte usada em um balão de palavra tem o estilo tachado definido.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*
</dt> <dd>

O endereço de um valor que receberá **True se o** estilo tachado da fonte estiver definido e **False** se não.

</dd> </dl>

O estilo de fonte usado em um balão de palavra de caractere é definido no Editor de Caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode substituir as configurações de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

 

 




