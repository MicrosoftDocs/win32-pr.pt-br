---
title: GetStyle IAgentBalloonEx
description: GetStyle IAgentBalloonEx
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822823"
---
# <a name="iagentballoonexgetstyle"></a>IAgentBalloonEx:: GetStyle

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

Recupera as configurações de estilo de balão de palavras do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*
</dt> <dd>

Configurações de estilo para o balão do Word, que pode ser uma combinação de qualquer um dos seguintes valores:



| Valor                                                                           | Descrição                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| balão de estilo de balão **curto sem sinal const** **\_ \_ = 0x00000001;**<br/> | O balão tem suporte para saída.                        |
| const estilo de balão **curto não assinado** **\_ \_ SIZETOTEXT = 0x0000002;**           | A altura do balão é dimensionada para acomodar a saída do texto. |
| **const-** **AutoOcultar estilo de balão não assinado constante \_ \_ = 0x00000004;**            | O balão é ocultado automaticamente.                        |
| **const não assinada estilo curto** de **balão \_ \_ autoritmo = 0x00000008;**            | A saída do texto é peratualizada com base na taxa de saída.          |



 

</dd> </dl>

Quando o bit do estilo de **balão** é definido, o balão de palavra é exibido quando o método [**Speak**](speak-method.md) ou [**Think**](think-method.md) é usado, a menos que o usuário substitua sua exibição por meio da folha de propriedades do Microsoft Agent. Quando não definido, nenhum balão é exibido.

Quando o bit do estilo **SizeToText** é definido, o balão do Word dimensiona automaticamente a altura do balão para o tamanho atual do texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) . Quando não definido, a altura do balão é baseada na configuração da propriedade número de linhas do balão. Esse bit de estilo é definido como 1 e uma tentativa de usar [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) resultará em um erro.

Quando o bit do estilo de **AutoOcultar** é definido, o balão de palavras é ocultado automaticamente após um curto tempo limite. Quando não definido, o balão é exibido até uma nova chamada de [**fala**](speak-method.md) ou [**reflexão**](think-method.md) , o caractere é ocultado ou o usuário clica ou arrasta o caractere.

Quando o bit do estilo do **autoritmo** é definido, o balão do Word ultrapassa a saída com base na taxa de saída atual, por exemplo, uma palavra por vez. Quando a saída excede o tamanho do balão, o texto anterior é rolado automaticamente. Quando não definido, todo o texto incluído em uma instrução de [**fala**](speak-method.md) ou de [**reflexão**](think-method.md) é exibido de uma vez.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

Os padrões para esses bits de estilo se baseiam nas configurações quando o caractere é compilado por meio do editor de caracteres do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloonEx:: SetStyle**](iagentballoonex--setstyle.md)


 

 





