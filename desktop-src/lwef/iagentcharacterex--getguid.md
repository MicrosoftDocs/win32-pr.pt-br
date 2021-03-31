---
title: GetGUID IAgentCharacterEx
description: GetGUID IAgentCharacterEx
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916475"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx:: GetGuid

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

Recupera a ID exclusiva para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*
</dt> <dd>

Endereço de um BSTR que recebe a ID para o caractere.

</dd> </dl>

A propriedade retorna uma representação de cadeia de caracteres do GUID (formatado com chaves e traços) que o servidor usa para identificar exclusivamente o caractere. Um identificador de caractere é definido quando é compilado com o editor de caracteres do Microsoft Agent. a propriedade é somente leitura.

 

 




