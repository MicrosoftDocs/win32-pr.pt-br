---
description: Descreve como criar um objeto PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Criando um objeto PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781429"
---
# <a name="creating-a-peninputpanel-object"></a>Criando um objeto PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) e [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)). Consulte a [programação do painel de entrada de texto](programming-the-text-input-panel.md).\]

Os construtores de código gerenciado fornecem uma maneira conveniente de criar um objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) e anexá-lo a um controle em uma única etapa. Este \# exemplo C cria um objeto PenInputPanel e o anexa a um controle [InkEdit](/previous-versions/ms835842(v=msdn.10)) existente, `InkEdit1` com uma linha de código.


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



O mesmo exemplo em Visual Basic .NET tem esta aparência:


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



Essa técnica é útil em casos em que um objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) será associado a um único controle durante seu tempo de vida. Nos casos em que você deseja usar um objeto PenInputPanel e associá-lo a vários controles, como demonstrado no [exemplo de PenInputPanel](peninputpanel-sample.md), use a propriedade [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) para alterar o controle ao qual o objeto PenInputPanel está associado.

Para anexar um objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a um controle sem usar um construtor, use a propriedade [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) . Use essa técnica para idiomas que não dão suporte aos construtores gerenciados, como C++.

 

 
