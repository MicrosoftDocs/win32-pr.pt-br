---
description: Descrição de técnicas de subpadrão para expor controles personalizados.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Técnicas de subpadrão para expor controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812795"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Técnicas de subpadrão para expor controles personalizados

Se um aplicativo não oferecer suporte ao Microsoft Acessibilidade Ativa, ele poderá não estar totalmente acessível. As técnicas a seguir renderizam os controles parcialmente compatíveis:

-   Retornar uma cadeia de caracteres descritiva quando o controle for consultado usando a \_ mensagem de gettext do WM. Por exemplo, permita que um equivalente personalizado de um controle de botão rotulado como "Print" para retornar a cadeia de caracteres "botão Imprimir". Isso identifica o tipo de controle e o rótulo. A mesma cadeia de caracteres é apropriada para um botão com um rótulo que seja algo diferente de texto, como um gráfico de uma impressora. Da mesma forma, permita que um controle personalizado se comporta como uma caixa de seleção para retornar a cadeia de caracteres de legenda "caixa de seleção de impressão habilitada, marcada".
-   Dê suporte à \_ mensagem do WM GETDLGCODE, identificando a entrada do teclado com suporte. Por exemplo, permita que um equivalente personalizado de um controle de edição manipule \_ o WM GETDLGCODE retornando DLGC \_ HASSETSEL se ele tratar as mensagens para definir a seleção, DLGC \_ WANTARROWS se usar as teclas de direção e DLGC \_ WANTCHARS para indicar que ela usa a entrada de caracteres.
    > [!Note]  
    > Somente controles que têm seus próprios identificadores de janela podem responder às \_ mensagens do WM gettext e do WM \_ GETDLGCODE.

     

Para evitar problemas de compatibilidade com auxílios de acessibilidade, você deve seguir as diretrizes de Acessibilidade Ativa de acordo ao criar controles personalizados. Para obter mais informações sobre como evitar problemas de compatibilidade com auxílios de acessibilidade, consulte a seção [acessibilidade](../accessibility/accessibility.md) .

 

 
