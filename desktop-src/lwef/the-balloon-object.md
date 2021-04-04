---
title: O objeto de balão
description: O objeto de balão
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161943"
---
# <a name="the-balloon-object"></a>O objeto de balão

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O Microsoft Agent dá suporte à legenda textual do método [**Speak**](speak-method.md) usando um balão de palavras de desenho. O método [**Think**](think-method.md) permite que você exiba texto sem saída de áudio em um balão de palavras "pensados".

Os padrões da janela de balão inicial de um caractere são definidos e compilados no editor de caracteres do Microsoft Agent. Uma vez em execução, as propriedades de [**fonte**](https://www.bing.com/search?q=**Font**) e [**habilitadas**](enabled-property.md) do balão podem ser substituídas pelo usuário. Se um usuário alterar as propriedades do balão do Word, eles afetarão todos os caracteres. Os balões de [**fala**](speak-method.md) e de palavra de [**opinião**](think-method.md) usam as mesmas configurações de propriedade para tamanho. Você pode acessar as propriedades do balão de palavras de um caractere por meio do objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) , que é um filho do objeto [**Character**](/windows/desktop/lwef/the-characters-object) .

O objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) dá suporte às seguintes propriedades:

-   [**Fundo**](backcolor-property.md)
-   [**BorderColor**](bordercolor-property.md)
-   [**CharsPerLine**](charsperline-property.md)
-   [**habilitado**](enabled-property.md)
-   [**FontCharSet**](fontcharset-property.md)
-   [**FontName**](fontname-property-bal.md)
-   [**FontBold**](fontbold-property.md)
-   [**FontItalic**](fontitalic-property.md)
-   [**FontSize**](fontsize-property-bal.md)
-   [**FontStrikeThru**](fontstrikethru-property.md)
-   [**FontUnderline**](fontunderline-property.md)
-   [**ForeColor**](forecolor-property.md)
-   [**NumberOfLines**](numberoflines-property.md)
-   [**Estilo**](style-property.md)
-   [**Visible**](visible-property-bal.md)

 

 