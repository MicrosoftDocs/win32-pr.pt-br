---
title: Usando barras de rolagem
description: Esta seção contém tópicos que demonstram como criar barras de rolagem.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d602426bd5f716a380d43104046f330d3240d516
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008458"
---
# <a name="using-scroll-bars"></a>Usando barras de rolagem

Esta seção contém tópicos que demonstram como criar barras de rolagem.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como criar barras de rolagem](create-scroll-bars.md)<br/>                                                                     | Ao criar uma janela sobreposta, pop-up ou filho, você pode adicionar barras de rolagem padrão usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especificando WS \_ HSCROLL, WS \_ VSCROLL ou ambos os estilos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Como rolar o texto](scroll-text-in-scroll-bars.md)<br/>                                                                    | Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que um usuário Role o texto. O exemplo nesta seção cria e exibe uma matriz de cadeias de caracteres de texto e processa mensagens de barra de rolagem do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) para que o usuário possa rolar o texto vertical e horizontalmente. <br/>                                                                                                                                                                                                                                                                 |
| [Como rolar um bitmap](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que o usuário Role um bitmap. <br/> O exemplo inclui um item de menu que copia o conteúdo da tela para um bitmap e exibe o bitmap na área do cliente. O exemplo também processa as mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) que são geradas pelas barras de rolagem para que o usuário possa rolar o bitmap horizontalmente e verticalmente. Ao contrário do exemplo de texto rolado, o exemplo de bitmap emprega a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para desenhar a parte inválida da área do cliente. <br/> |
| [Como criar uma interface de teclado para barras de rolagem padrão](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Embora um controle de barra de rolagem forneça uma interface de teclado interna, uma barra de rolagem padrão não. Para implementar uma interface de teclado para uma barra de rolagem padrão, um procedimento de janela deve processar a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e examinar o código de chave virtual especificado pelo parâmetro *wParam* . Se o código de chave virtual corresponder a uma tecla de direção, o procedimento de janela enviará a si mesmo uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com a palavra de ordem inferior do parâmetro *wParam* definido como o código de solicitação da barra de rolagem apropriada. <br/>                                              |



 

 

