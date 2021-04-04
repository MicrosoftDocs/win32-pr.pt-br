---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084133"
---
# <a name="iagentcharactergetextradata"></a>IAgentCharacter::GetExtraData

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

Recupera dados adicionais armazenados como parte do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*
</dt> <dd>

O endereço de um BSTR que recebe o valor dos dados adicionais para o caractere. Os dados adicionais de um caractere são definidos quando compilados com o editor de caracteres do Microsoft Agent. Um desenvolvedor de caracteres pode fornecer essa cadeia de caracteres editando o. Arquivo ad para um caractere. A configuração é opcional e pode não ser fornecida para todos os caracteres, nem os dados podem ser definidos ou alterados em tempo de execução. Além disso, o significado dos dados fornecidos é definido pelo desenvolvedor de caracteres.

</dd> </dl>

 

 




