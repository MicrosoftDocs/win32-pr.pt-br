---
title: Usando barras de rolagem
description: Esta seção contém tópicos que demonstram como criar barras de rolagem.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96b1341e76b80e4ba5bf45df3dcfee03db87bb82adb4ba50273edbac6db4ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957585"
---
# <a name="using-scroll-bars"></a>Usando barras de rolagem

Esta seção contém tópicos que demonstram como criar barras de rolagem.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como criar barras de rolagem](create-scroll-bars.md)<br/>                                                                     | Ao criar uma janela sobreboçada, pop-up ou filho, você pode adicionar barras de rolagem padrão usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especificando WS \_ HSCROLL, WS VSCROLL ou ambos os \_ estilos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Como rolar texto](scroll-text-in-scroll-bars.md)<br/>                                                                    | Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que um usuário role o texto. O exemplo nesta seção cria e exibe uma matriz de cadeias de caracteres de texto e processa mensagens de barra de rolagem [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) para que o usuário possa rolar o texto vertical e horizontalmente. <br/>                                                                                                                                                                                                                                                                 |
| [Como rolar um bitmap](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que o usuário role um bitmap. <br/> O exemplo inclui um item de menu que copia o conteúdo da tela para um bitmap e exibe o bitmap na área do cliente. O exemplo também processa as [**mensagens WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) geradas pelas barras de rolagem para que o usuário possa rolar o bitmap horizontal e verticalmente. Ao contrário do exemplo de texto rolado, o exemplo de bitmap emprega a [**função BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para desenhar a parte inválida da área do cliente. <br/> |
| [Como criar uma interface de teclado para barras de rolagem padrão](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Embora um controle de barra de rolagem fornece uma interface de teclado integrado, uma barra de rolagem padrão não fornece. Para implementar uma interface de teclado para uma barra de rolagem padrão, um procedimento de janela deve processar a mensagem [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e examinar o código de chave virtual especificado pelo *parâmetro wParam.* Se o código de chave virtual corresponder a uma tecla de seta, o procedimento de janela enviará uma mensagem [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) com a palavra de ordem baixa do *parâmetro wParam* definida como o código de solicitação de barra de rolagem apropriado. <br/>                                              |



 

 

