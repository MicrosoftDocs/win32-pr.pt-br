---
title: Como implementar dicas de In-Place ferramentas
description: As dicas de ferramenta in-locar são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados. Para ver uma ilustração, consulte Sobre controles de dica de ferramenta.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd3b01d30a20b52cbb80121cc8c1d793965acf0ea3cf4f2be1ce4553f4ccb98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671720"
---
# <a name="how-to-implement-in-place-tooltips"></a>Como implementar dicas de In-Place ferramentas

As dicas de ferramenta in-locar são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados. Para ver uma ilustração, consulte [Sobre controles de dica de ferramenta](tooltip-controls.md).

A diferença entre dicas de ferramenta comuns e in-place é o posicionamento. Por padrão, quando o ponteiro do mouse passar o mouse sobre uma região que tem uma dica de ferramenta associada a ele, a dica de ferramenta será exibida adjacente à região. No entanto, as dicas de ferramenta são janelas e podem ser posicionadas em qualquer lugar que você escolher chamando [**SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) Criar uma dica de ferramenta in-loque é uma questão de posicionar a janela de dica de ferramenta para que ela sobrepõe a cadeia de caracteres de texto.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="positioning-an-in-place-tooltip"></a>Posicionando uma dica In-Place Tooltip

Você precisa manter o controle de três retângulos ao posicionar uma dica de ferramenta in-locar:

1.  O retângulo que envolve o texto completo do rótulo.
2.  O retângulo que envolve o texto da dica de ferramenta. O texto da dica de ferramenta é idêntico ao texto completo do rótulo e normalmente é do mesmo tamanho e fonte. Os dois retângulos de texto geralmente terão o mesmo tamanho.
3.  O retângulo da janela de dica de ferramenta. Esse retângulo é um pouco maior do que o retângulo de texto da dica de ferramenta que ele inclui.


Os três retângulos são mostrados dinamicamente na ilustração a seguir. A parte oculta do texto do rótulo é indicada por uma plano de fundo cinza.

![diagrama mostrando uma cadeia de caracteres longa, metade das quais tem uma tela de fundo cinza e, em seguida, a mesma cadeia de caracteres dentro de um retângulo de janela de dica de ferramenta maior](images/inplace.png)

Para criar uma dica de ferramenta in-loque, você deve posicionar o retângulo de texto da dica de ferramenta para que ele sobrepõe o retângulo de texto do rótulo. O procedimento para alinhar os dois retângulos é relativamente simples:

1.  Defina o retângulo de texto do rótulo.
2.  Posiciona a janela de dica de ferramenta para que o retângulo de texto da dica de ferramenta sobrepõe o retângulo de texto do rótulo.


Na prática, geralmente é suficiente alinhar o canto superior esquerdo dos dois retângulos de texto. Tentar ressalizar o retângulo de texto da dica de ferramenta para corresponder exatamente ao retângulo de texto do rótulo pode causar problemas com a exibição da dica de ferramenta.

O problema com esse esquema simples é que você não pode posicionar o retângulo de texto da dica de ferramenta diretamente. Em vez disso, você deve posicionar o retângulo da janela de dica de ferramenta apenas muito acima e à esquerda do retângulo de texto do rótulo para que os cantos dos dois retângulos de texto coincidam. Em outras palavras, você precisa saber o deslocamento entre o retângulo da janela de dica de ferramenta e seu retângulo de texto delimitado. Em geral, não há uma maneira simples de determinar esse deslocamento.

### <a name="implement-in-place-tooltips"></a>Implementar In-Place tooltips

O fragmento de código a seguir ilustra como usar uma mensagem [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) em um manipulador [TTN \_ SHOW](ttn-show.md) para exibir uma dica de ferramenta in-loquete. Seu aplicativo indica que o texto do rótulo é truncado definindo a *variável fMyStringIsTruncated* privada como **TRUE.** O manipulador chama uma função definida pelo aplicativo, **GetMyItemRect,** para recuperar o retângulo de texto do rótulo. Esse retângulo é passado para o controle de dica de ferramenta **com TTM \_ ADJUSTRECT**, que retorna o retângulo da janela correspondente. [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) é chamado para posicionar a dica de ferramenta sobre o rótulo.


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



Este exemplo não altera o tamanho da dica de ferramenta, apenas sua posição. Os dois retângulos de texto são alinhados em seus cantos superiores esquerdos, mas não necessariamente com as mesmas dimensões. Na prática, a diferença geralmente é pequena e essa abordagem é recomendada para a maioria das finalidades. Embora você possa, em princípio, usar [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para reorganizar, bem como reposicionar a dica de ferramenta, isso pode ter consequências imprevisíveis.

## <a name="remarks"></a>Comentários

Controles [comuns versão 5.80](common-control-versions.md) simplifica o uso de dicas de ferramenta in-loque pela adição de uma nova mensagem, [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md). Envie essa mensagem com as coordenadas do retângulo de texto do rótulo que você deseja que a dica de ferramenta sobrepor e retorne as coordenadas de um retângulo de janela de dica de ferramenta posicionado adequadamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 

 