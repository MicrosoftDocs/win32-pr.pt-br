---
title: GetGUID IAgentCharacterEx
description: GetGUID IAgentCharacterEx
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e43a98617b1e2d25a25167ad5b95462eeb462f40f5a353b5a5ec45ffb3a9cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477964"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx:: GetGuid

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

 




