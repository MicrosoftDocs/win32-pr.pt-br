---
title: IAgentCharacterEx think
description: IAgentCharacterEx think
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a513a070104605df0cf3e0e722852a2b68d5845f4bcdb1ef6073954b3f9a18c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105434"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx:: think

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Exibe o balão de palavras pensadas do caractere com o texto especificado.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

O texto a ser exibido no balão de pensamento do caractere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de **reflexão** .

</dd> </dl>

Assim como o método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) , o método **Think** é uma solicitação em fila que exibe o texto em um balão de palavras, exceto que as ideias são exibidas em um balão de pensamento especial. O balão de pensamento dá suporte apenas à marca de controle de fala de indicador (**\\ mrk**) e ignora quaisquer outras marcas de controle de fala. Ao contrário de **IAgentCharacter:: Speak**, o método **Think** não altera o estado de animação do caractere.

As configurações de [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) também se aplicam ao estilo de aparência do balão de pensamento. Por exemplo, a propriedade [**habilitada**](enabled-property.md) do balão também deve ser **verdadeira** para o texto a ser exibido.

A quebra automática de palavras do Microsoft Agent no balão de palavras quebra palavras usando caracteres de espaço em branco (por exemplo, espaço e tabulação). No entanto, ele pode quebrar uma palavra para se ajustar também ao balão. Em linguagens como japonês, chinês e tailandês, em que espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.

> [!Note]  
> Defina a ID de idioma do caractere (usando [**IAgentCharacterEx:: Setlanguageid**](iagentcharacterex--setlanguageid.md) antes de usar o método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) para garantir a exibição de texto apropriada dentro do balão do Word.

 

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: Gethabilited**](iagentballoon--getenabled.md), [**IAgentBalloonEx:: SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md)


 

 