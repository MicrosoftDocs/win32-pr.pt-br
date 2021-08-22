---
description: Descreve o uso do objeto PenInputPanel com caixas de combinação.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Usando o PenInputPanel com caixas de combinação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1e90d581e08f9a23346bbf13cf8c3866f6e947f1d9b23375248f3ba9c8636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589296"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Usando o PenInputPanel com caixas de combinação

\[O [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) foi substituído por [Microsoft.Ink.TextInput.](/previous-versions/ms581554(v=vs.100)) Consulte Programando o [painel de entrada de texto.](programming-the-text-input-panel.md)\]

Se você anexar um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a um controle [ComboBox,](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) toque na caneta do tablet na caixa de combinação da parte do controle de edição em runtime, o objeto PenInputPanel não será exibido. No entanto, ele será exibido se você tocar na seta para baixo. Isso porque a janela do controle de edição na caixa de combinação não é a janela que recebe mensagens de caneta. As caixas de combinação têm uma janela de edição filho. A solução para esse problema é determinar se a janela à qual o objeto PenInputPanel está anexado tem uma janela filho. Se sim, você pode anexar o objeto PenInputPanel à janela filho.

Definir a [propriedade VerticalOffset](/previous-versions/ms571983(v=vs.100)) do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) como um valor de -1 faz com que o painel apareça na parte superior da caixa de combinação.

 

 
