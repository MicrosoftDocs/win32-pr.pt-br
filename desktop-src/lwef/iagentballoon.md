---
title: IAgentBalloon
description: IAgentBalloon
ms.assetid: 94a48cd9-bea5-4993-8991-50c6c86a646b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b811956e368abbaf2d2782c68017084f5e17a09f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640667"
---
# <a name="iagentballoon"></a>IAgentBalloon

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgentBalloon** define uma interface que permite que os aplicativos consultem Propriedades para o balão do Microsoft Agent Word. Essas funções também estão disponíveis em [**IAgentBalloonEx**](https://www.bing.com/search?q=**IAgentBalloonEx**).

Os padrões iniciais para o balão de palavras de um caractere são definidos no editor de caracteres do Microsoft Agent, mas depois que o aplicativo estiver em execução, o usuário poderá substituir as propriedades de [Font](fontname-property.md) e [**Enabled**](enabled-property.md) . Se um usuário alterar as propriedades do balão, a alteração afetará todos os caracteres. As propriedades do objeto [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) também se aplicam à saída de texto por meio do método [**Think**](think-method.md) .

**Métodos em ordem vtable**



| Métodos IAgentBalloon                                       | Description                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [GetEnabled](iagentballoon--getenabled.md)                 | Retorna se o balão de palavra está habilitado.                                          |
| [GetNumLines](iagentballoon--getnumlines.md)               | Retorna o número de linhas exibidas na palavra balão.                            |
| [GetNumCharsPerLine](iagentballoon--getnumcharsperline.md) | Retorna o número médio de caracteres por linha exibidos na palavra balão.      |
| [GetFontName](iagentballoon--getfontname.md)               | Retorna o nome da fonte exibida na palavra balão.                           |
| [GetFontSize](iagentballoon--getfontsize.md)               | Retorna o tamanho da fonte exibida na palavra balão.                           |
| [GetFontBold](iagentballoon--getfontbold.md)               | Retorna se a fonte exibida na palavra balão está em negrito.                       |
| [GetFontItalic](iagentballoon--getfontitalic.md)           | Retorna se a fonte exibida na palavra balão está em itálico.                     |
| [GetFontStrikethru](iagentballoon--getfontstrikethru.md)   | Retorna se a fonte exibida no balão de palavra é exibida como tachada. |
| [GetFontUnderline](iagentballoon--getfontunderline.md)     | Retorna se a fonte exibida no balão de palavra é sublinhada.                 |
| [GetForeColor](iagentballoon--getforecolor.md)             | Retorna a cor de primeiro plano exibida na palavra balão.                           |
| [GetBackColor](iagentballoon--getbackcolor.md)             | Retorna a cor do plano de fundo exibida na palavra balão.                           |
| [Getbordercolor](iagentballoon--getbordercolor.md)         | Retorna a cor da borda exibida na palavra balão.                               |
| [Não visível](iagentballoon--setvisible.md)                 | Define o balão de palavras como visível.                                                  |
| [GetVisible](iagentballoon--getvisible.md)                 | Retorna a configuração de visibilidade para o balão de palavras.                                  |
| [Setnomedafonte](iagentballoon--setfontname.md)               | Define a fonte usada no balão de palavras.                                               |
| [Setfontize](iagentballoon--setfontsize.md)               | Define o tamanho da fonte usado no balão de palavras.                                          |
| [SetFontCharSet](iagentballoon--setfontcharset.md)         | Define o conjunto de caracteres usado no balão de palavras.                                      |
| [GetFontCharSet](iagentballoon--getfontcharset.md)         | Retorna o conjunto de caracteres usado no balão de palavras.                                   |



 

 

 