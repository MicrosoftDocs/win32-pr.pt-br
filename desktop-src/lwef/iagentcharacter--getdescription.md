---
title: Getdescrição do IAgentCharacter
description: Getdescrição do IAgentCharacter
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364505"
---
# <a name="iagentcharactergetdescription"></a>IAgentCharacter:: GetDescription

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

O endereço de um BSTR que recebe o valor da descrição para o caractere. A descrição de um caractere é definida quando é compilada com o editor de caracteres do Microsoft Agent. A configuração descrição é opcional e pode não ser fornecida para todos os caracteres.

</dd> </dl>

 

 




