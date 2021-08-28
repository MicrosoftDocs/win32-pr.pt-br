---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757b2d7554f1efcee27a519b9df61b4601a237b557c3aa26b6575864144a2850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105232"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

O nome da fonte retornado corresponde à fonte usada para exibir texto no menu pop-up do caractere quando o aplicativo cliente está ativo de entrada. O valor padrão para a configuração de fonte baseia-se na configuração de fonte de menu para a configuração de ID de idioma do caractere ou, se não estiver definido, a configuração de ID de idioma padrão do usuário.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




