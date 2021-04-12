---
title: IAgentCommandsEx getnomedafonte
description: IAgentCommandsEx getnomedafonte
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364106"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx:: getnomedafonte

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Recupera o valor da fonte exibida no menu pop-up do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

O endereço de um BSTR que recebe o nome da fonte exibido no menu pop-up do caractere.

</dd> </dl>

O nome da fonte retornado corresponde à fonte usada para exibir o texto no menu pop-up do caractere quando o aplicativo cliente é de entrada-ativo. O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere ou, se não estiver definido, a configuração de ID de idioma padrão do usuário.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: setnomedafonte**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx:: setfontize**](iagentcommandsex--setfontsize.md)


 

 




