---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23216f1a7b013a54de1e64351c2a9d3a3d3359d90e0516cd6852a003baa047c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716186"
---
# <a name="iagentcharactergetdescription"></a>IAgentCharacter::GetDescription

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Recupera a descrição do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*
</dt> <dd>

O endereço de um BSTR que recebe o valor da descrição do caractere. A descrição de um caractere é definida quando ele é compilado com o Editor de Caracteres do Microsoft Agent. A configuração de descrição é opcional e pode não ser fornecida para todos os caracteres.

</dd> </dl>

 

 




