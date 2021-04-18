---
description: Use controles padrão do Windows sempre que possível, pois eles são totalmente compatíveis com as diretrizes de Acessibilidade Ativa da Microsoft. Isso inclui controles fornecidos pelo Windows (User32.dll) e pela biblioteca de controles comuns do Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Usando controles padrão do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296306"
---
# <a name="using-standard-windows-controls"></a>Usando controles padrão do Windows

Use controles padrão do Windows sempre que possível, pois eles são totalmente compatíveis com as diretrizes de Acessibilidade Ativa da Microsoft. Isso inclui controles fornecidos pelo Windows (User32.dll) e pela biblioteca de controles comuns do Windows (Comctl32.dll).

Cada controle padrão do Windows é uma janela separada de uma classe específica, portanto, o auxílio de acessibilidade é notificado quando o foco é movido para um novo controle. O auxílio pode determinar a classe da janela de controles e todas as mensagens adicionais que ele pode enviar para consultar ou alterar o estado dos controles. O auxílio também pode identificar todos os controles filho contidos em uma janela pai e identificar o pai de qualquer controle.

Alguns controles comuns são extremamente flexíveis e, muitas vezes, podem substituir controles personalizados menos acessíveis e controles desenhados pelo proprietário. Por exemplo, um modo de exibição de lista pode substituir uma caixa de listagem desenhada pelo proprietário para exibir uma caixa de seleção ao lado de cada item. Como outro exemplo, o controle de botão avançado pode exibir imagens e texto. Anteriormente, isso exigia o uso de um controle personalizado.

 

 



