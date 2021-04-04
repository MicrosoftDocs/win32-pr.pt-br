---
title: Como implementar dicas de ferramentas de In-Place
description: Dicas de ferramenta in-loco são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados. Para obter uma ilustração, consulte sobre os controles de dica de ferramenta.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008626"
---
# <a name="how-to-implement-in-place-tooltips"></a>Como implementar dicas de ferramentas de In-Place

Dicas de ferramenta in-loco são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados. Para obter uma ilustração, consulte [sobre os controles de dica de ferramenta](tooltip-controls.md).

A diferença entre as dicas de ferramenta comuns e no local é o posicionamento. Por padrão, quando o ponteiro do mouse passa sobre uma região que tem uma dica de ferramenta associada a ela, a dica de ferramenta é exibida adjacente à região. No entanto, as dicas de ferramentas são janelas e podem ser posicionadas em qualquer lugar que você escolher chamando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). A criação de uma dica de ferramenta in-loco é uma questão de posicionar a janela de dica de ferramenta para que ela se sobreponha à cadeia de texto.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="positioning-an-in-place-tooltip"></a>Posicionando uma dica de ferramenta In-Place

Você precisa manter o controle de três retângulos ao posicionar uma dica de ferramenta in-loco:

1.  O retângulo que circunda o texto do rótulo completo.
2.  O retângulo que circunda o texto da dica de ferramenta. O texto da dica de ferramenta é idêntico ao texto completo do rótulo e normalmente tem o mesmo tamanho e fonte. Portanto, os dois retângulos de texto geralmente terão o mesmo tamanho.
3.  O retângulo da janela de dica de ferramenta. Esse retângulo é um pouco maior do que o retângulo de texto de dica de ferramenta que ele fecha.


Os três retângulos são mostrados esquemáticomente na ilustração a seguir. A parte oculta do texto do rótulo é indicada por um plano de fundo cinza.

![diagrama mostrando uma cadeia de caracteres longa, metade dela tem um plano de fundo cinza e, em seguida, a mesma cadeia de caracteres em um retângulo de janela de dica de ferramenta maior](images/inplace.png)

Para criar uma dica de ferramenta in-loco, você deve posicionar o retângulo de texto da dica de ferramenta para que ele se sobreponha ao retângulo do texto do rótulo. O procedimento para alinhar os dois retângulos é relativamente simples:

1.  Defina o retângulo do texto do rótulo.
2.  Posicione a janela de dica de ferramenta para que o retângulo de texto de dica de ferramenta sobreponha o retângulo de texto do rótulo.


Na prática, geralmente é suficiente alinhar o canto superior esquerdo dos dois retângulos de texto. A tentativa de redimensionar o retângulo de texto da dica de ferramenta para corresponder exatamente ao retângulo do texto do rótulo pode causar problemas com a exibição da dica de ferramenta.

O problema com esse esquema simples é que você não pode posicionar o retângulo de texto de dica de ferramenta diretamente. Em vez disso, você deve posicionar o retângulo da janela de dica de ferramenta exatamente o suficiente acima e à esquerda do retângulo de texto do rótulo para que os cantos dos dois retângulos de texto coincidam. Em outras palavras, você precisa saber o deslocamento entre o retângulo da janela de dica de ferramenta e seu retângulo de texto embutido. Em geral, não há uma maneira simples de determinar esse deslocamento.

### <a name="implement-in-place-tooltips"></a>Implementar dicas de ferramentas de In-Place

O fragmento de código a seguir ilustra como usar uma mensagem [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) em um manipulador [TTN \_ show](ttn-show.md) para exibir uma dica de ferramenta in-loco. Seu aplicativo indica que o texto do rótulo está truncado definindo a variável *fMyStringIsTruncated* privada como **true**. O manipulador chama uma função definida pelo aplicativo, **GetMyItemRect**, para recuperar o retângulo de texto do rótulo. Esse retângulo é passado para o controle ToolTip com **TTM \_ ADJUSTRECT**, que retorna o retângulo de janela correspondente. Em seguida, [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) é chamado para posicionar a dica de ferramenta sobre o rótulo.


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



Este exemplo não altera o tamanho da dica de ferramenta, apenas sua posição. Os dois retângulos de texto estão alinhados em seus cantos superior esquerdo, mas não necessariamente com as mesmas dimensões. Na prática, a diferença é geralmente pequena e essa abordagem é recomendada para a maioria das finalidades. Embora você possa, em princípio, usar [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para redimensionar e reposicionar a dica de ferramenta, fazer isso pode ter consequências imprevisíveis.

## <a name="remarks"></a>Comentários

Os controles comuns [versão 5,80](common-control-versions.md) simplificam o uso de dicas de ferramenta in-loco pela adição de uma nova mensagem, [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md). Envie essa mensagem com as coordenadas do retângulo de texto do rótulo que você deseja que a dica de ferramenta sobreponha e retorne as coordenadas de um retângulo de janela de dica de ferramenta posicionado adequadamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 

 