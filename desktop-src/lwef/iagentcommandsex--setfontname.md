---
title: IAgentCommandsEx setnomedafonte
description: IAgentCommandsEx setnomedafonte
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511425df848749791d2803a484e00da8e838cfa191eade05c578fdad4b3ca6cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105192"
---
# <a name="iagentcommandsexsetfontname"></a>IAgentCommandsEx:: setnomedafontename

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

Define a fonte exibida no menu pop-up do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

Um BSTR que define a fonte exibida no menu pop-up do caractere.

</dd> </dl>

Essa propriedade determina a fonte usada para exibir o texto no menu pop-up do caractere. O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere-ou se não estiver definido, a configuração de ID de idioma padrão do usuário.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: getnomedafonte**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: getfonts**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: setfontize**](iagentcommandsex--setfontsize.md)


 

 




