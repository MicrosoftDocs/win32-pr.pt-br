---
description: Descrição de técnicas subpadradas para expor controles personalizados.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Técnicas subpadradas para expor controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121856bf5303b011b785a26bc47013e0df93463d7f278d6e4586991a47d8e020
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934306"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Técnicas subpadradas para expor controles personalizados

Se um aplicativo não dá suporte Microsoft Active Accessibility, ele pode não estar totalmente acessível. As técnicas a seguir renderizarão controles parcialmente compatíveis:

-   Retornar uma cadeia de caracteres descritiva quando o controle for consultado usando a mensagem WM \_ GETTEXT. Por exemplo, permita que um equivalente personalizado de um controle de botão rotulado como "Imprimir" retorne a cadeia de caracteres "Botão imprimir". Isso identifica o tipo de controle e o rótulo. A mesma cadeia de caracteres é apropriada para um botão com um rótulo diferente de texto, como um gráfico de uma impressora. Da mesma forma, permita que um controle personalizado que se comporte como uma caixa de seleção retorne a cadeia de caracteres de legenda "Caixa de seleção Impressão Habilitada, marcada".
-   Suporte à mensagem WM \_ GETDLGCODE, identificando a entrada do teclado com suporte. Por exemplo, permita um equivalente personalizado de um controle de edição para manipular WM GETDLGCODE retornando DLGC HASSETSEL se ele manipular mensagens para definir a \_ seleção, DLGC WANTARROWS se ele usar teclas de direção e \_ \_ DLGC WANTCHARS para indicar que ele usa a entrada \_ de caracteres.
    > [!Note]  
    > Somente os controles que têm seus próprios alças de janela podem responder às mensagens WM GETTEXT e \_ WM \_ GETDLGCODE.

     

Para evitar problemas de compatibilidade com auxiliares de acessibilidade, você deve seguir Acessibilidade Ativa diretrizes ao criar controles personalizados. Para obter mais informações sobre como evitar problemas de compatibilidade com auxiliares de acessibilidade, consulte a [seção Acessibilidade.](../accessibility/accessibility.md)

 

 
