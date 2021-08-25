---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107e6fdb6be3e79dee14177d9f56ee7d258f3455d578641e7d3a3b3cf044c741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962266"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter::GetName

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Recupera o nome do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

O endereço de um BSTR que recebe o valor do nome do caractere.

</dd> </dl>

O nome padrão de um caractere é definido quando ele é compilado com o Editor de Caracteres do Microsoft Agent. O nome de um caractere pode variar com base na ID de idioma do caractere. Os caracteres podem ser compilados com nomes diferentes para idiomas diferentes.

Você também pode definir o nome do caractere usando **IAgentCharacter:SetName**; no entanto, isso altera o nome de todos os clientes atuais do caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::SetName**](iagentcharacter--setname.md)


 

 




