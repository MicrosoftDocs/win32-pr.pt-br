---
title: IAgentCommandsEx getfontize
description: IAgentCommandsEx getfontize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364105"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx:: getfontize

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Recupera o valor do tamanho da fonte exibida no menu pop-up do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

O endereço de um valor que recebe o tamanho da fonte.

</dd> </dl>

O tamanho do ponto da fonte retornado corresponde ao tamanho definido para exibir o texto no menu pop-up do caractere quando o cliente está na entrada-ativo. O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere, ou se não estiver definido, a configuração de idioma padrão do usuário.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: setfonts**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx:: setnomedafontename**](iagentcommandsex--setfontname.md)


 

 




