---
description: Use controles de Windows padrão sempre que possível, pois eles são totalmente compatíveis com as diretrizes de Acessibilidade Ativa da Microsoft. isso inclui controles fornecidos por Windows (User32.dll) e a Windows biblioteca de controles comuns (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: usando controles de Windows padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71beab38b4ee6ea6472a34b4edb190deed97731496eac7101859a9340c65ad0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449269"
---
# <a name="using-standard-windows-controls"></a>usando controles de Windows padrão

Use controles de Windows padrão sempre que possível, pois eles são totalmente compatíveis com as diretrizes de Acessibilidade Ativa da Microsoft. isso inclui controles fornecidos por Windows (User32.dll) e a Windows biblioteca de controles comuns (Comctl32.dll).

cada controle de Windows padrão é uma janela separada de uma classe específica, portanto, o auxílio de acessibilidade é notificado quando o foco é movido para um novo controle. O auxílio pode determinar a classe da janela de controles e todas as mensagens adicionais que ele pode enviar para consultar ou alterar o estado dos controles. O auxílio também pode identificar todos os controles filho contidos em uma janela pai e identificar o pai de qualquer controle.

Alguns controles comuns são extremamente flexíveis e, muitas vezes, podem substituir controles personalizados menos acessíveis e controles desenhados pelo proprietário. Por exemplo, um modo de exibição de lista pode substituir uma caixa de listagem desenhada pelo proprietário para exibir uma caixa de seleção ao lado de cada item. Como outro exemplo, o controle de botão avançado pode exibir imagens e texto. Anteriormente, isso exigia o uso de um controle personalizado.

 

 



