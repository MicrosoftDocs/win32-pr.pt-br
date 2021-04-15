---
title: IAgentCommandsEx setfontize
description: IAgentCommandsEx setfontize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454000"
---
# <a name="iagentcommandsexsetfontsize"></a>IAgentCommandsEx:: setfontize

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Define o tamanho da fonte exibida no menu pop-up do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Tamanho da fonte.

</dd> </dl>

Essa propriedade determina o tamanho do ponto da fonte usada para exibir o texto no menu pop-up do caractere quando o aplicativo cliente é de entrada-ativo. O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere-ou se não estiver definido, a configuração de idioma padrão do usuário. Se não houver entrada-ativa, o texto da [](/windows/desktop/lwef/the-command-object) [**legenda**](caption-property.md) do comando do aplicativo cliente aparecerá no tamanho do ponto especificado para o cliente de entrada-ativo.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: Getfonte**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: getnomedafonte**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: setnomedafontename**](iagentcommandsex--setfontname.md)


 

 