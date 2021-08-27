---
title: O objeto de balão
description: O objeto de balão
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc2ad1256b040588121dcb92fc8f66fea540b3051b92a6fe5273eb2f81107b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745968"
---
# <a name="the-balloon-object"></a>O objeto de balão

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O Microsoft Agent dá suporte à legenda textual [**do método Speak**](speak-method.md) usando um balão de palavra de desenho. O [**método Think**](think-method.md) permite exibir texto sem saída de áudio em um balão de palavra "thought".

Os padrões da janela de balão de palavra inicial de um caractere são definidos e compilados no Editor de Caracteres do Microsoft Agent. Após a execução, as propriedades [**Enabled**](enabled-property.md) e [**Font**](https://www.bing.com/search?q=**Font**) do balão podem ser substituídos pelo usuário. Se um usuário altera as propriedades do balão de palavra, ele afeta todos os caracteres. Os balão de palavras [**Fale**](speak-method.md) e [**Pensar**](think-method.md) usam as mesmas configurações de propriedade para tamanho. Você pode acessar as propriedades do balão de palavra de um caractere por meio do objeto [**Balão,**](/windows/desktop/lwef/the-balloon-object) que é um filho do [**objeto**](/windows/desktop/lwef/the-characters-object) Character.

O [**objeto Balloon**](/windows/desktop/lwef/the-balloon-object) dá suporte às seguintes propriedades:

-   [**Backcolor**](backcolor-property.md)
-   [**BorderColor**](bordercolor-property.md)
-   [**CharsPerLine**](charsperline-property.md)
-   [**habilitado**](enabled-property.md)
-   [**Fontcharset**](fontcharset-property.md)
-   [**FontName**](fontname-property-bal.md)
-   [**FontBold**](fontbold-property.md)
-   [**FontItalic**](fontitalic-property.md)
-   [**FontSize**](fontsize-property-bal.md)
-   [**FontStrikeThru**](fontstrikethru-property.md)
-   [**FontUnderline**](fontunderline-property.md)
-   [**ForeColor**](forecolor-property.md)
-   [**NumberOfLines**](numberoflines-property.md)
-   [**Estilo**](style-property.md)
-   [**Visível**](visible-property-bal.md)

 

 