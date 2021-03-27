---
description: Você usa a função GetDC para executar o desenho que deve ocorrer instantaneamente em vez de quando uma \_ mensagem do WM Paint está sendo processada.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Usando a função GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967856"
---
# <a name="using-the-getdc-function"></a>Usando a função GetDC

Você usa a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para executar o desenho que deve ocorrer instantaneamente em vez de quando uma mensagem do [**WM \_ Paint**](wm-paint.md) está sendo processada. Esse desenho geralmente é em resposta a uma ação pelo usuário, como fazer uma seleção ou um desenho com o mouse. Nesses casos, o usuário deve receber comentários instantâneos e não deve ser forçado a parar de selecionar ou desenhar para que o aplicativo exiba o resultado. As seções a seguir mostram como usar o GetDC para desenhar em uma janela:

-   [Desenho com o mouse](drawing-with-the-mouse.md)
-   [Desenhando em intervalos de tempo](drawing-at-timed-intervals.md)

 

 



