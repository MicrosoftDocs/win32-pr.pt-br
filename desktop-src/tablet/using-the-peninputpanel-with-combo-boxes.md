---
description: Descreve como usar o objeto PenInputPanel com caixas de combinação.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Usando o PenInputPanel com caixas de combinação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647090"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Usando o PenInputPanel com caixas de combinação

\[O objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) foi substituído por [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)). Consulte a [programação do painel de entrada de texto](programming-the-text-input-panel.md).\]

Se você anexar um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a um controle [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , em seguida, toque na caneta do Tablet na caixa de combinação editar parte do controle em tempo de execução, o objeto PenInputPanel não será exibido. No entanto, ela será exibida se você tocar na seta suspensa. Isso ocorre porque a janela do controle de edição na caixa de combinação não é a janela que recebe mensagens de caneta. As caixas de combinação têm uma janela de edição filho. A solução para esse problema é determinar se a janela à qual o objeto PenInputPanel está anexado tem uma janela filho. Nesse caso, você pode anexar o objeto PenInputPanel à janela filho.

Definir a propriedade [VerticalOffset](/previous-versions/ms571983(v=vs.100)) do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) como um valor de-1 faz com que o painel apareça na parte superior da caixa de combinação.

 

 
