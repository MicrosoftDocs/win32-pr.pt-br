---
description: Visão geral da exibição do painel de entrada.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Exibindo o painel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782423"
---
# <a name="displaying-the-input-panel"></a>Exibindo o painel de entrada

\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) para código gerenciado). Consulte a [programação do painel de entrada de texto](programming-the-text-input-panel.md).\]

A ordem dos vários eventos de foco de um controle é a seguinte:

-   [Controle. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Controle. Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Controle. Validating](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Controle. validado](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control. LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

Não há nenhuma garantia de que o controle realmente tem o foco no momento em que a propriedade [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) é gravada quando é definida no manipulador de eventos [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) . O evento Control. Enter é o melhor lugar para anexar o objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a um controle, mas o evento [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) é o melhor local para alterar a propriedade [PenInputPanel. Visible](/previous-versions/ms571984(v=vs.100)) .

 

 
