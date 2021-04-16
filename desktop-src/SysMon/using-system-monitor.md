---
title: Usando o monitor do sistema
description: O monitor do sistema (SYSMON) pode ser incluído em qualquer aplicativo que dê suporte a ActiveX \ 174; controles. Por exemplo, você pode incluir o SYSMON em um aplicativo Microsoft Visual Basic ou em um documento HTML.
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754091"
---
# <a name="using-system-monitor"></a><span data-ttu-id="d52b8-104">Usando o monitor do sistema</span><span class="sxs-lookup"><span data-stu-id="d52b8-104">Using System Monitor</span></span>

<span data-ttu-id="d52b8-105">O monitor do sistema (SYSMON) pode ser incluído em qualquer aplicativo que ofereça suporte a controles ActiveX®.</span><span class="sxs-lookup"><span data-stu-id="d52b8-105">System Monitor (SYSMON) can be included in any application that supports ActiveX® controls.</span></span> <span data-ttu-id="d52b8-106">Por exemplo, você pode incluir o SYSMON em um aplicativo Microsoft Visual Basic ou em um documento HTML.</span><span class="sxs-lookup"><span data-stu-id="d52b8-106">For example, you can include SYSMON in a Microsoft Visual Basic application or in an HTML document.</span></span>

<span data-ttu-id="d52b8-107">O exemplo a seguir mostra como incluir o SYSMON em um documento HTML.</span><span class="sxs-lookup"><span data-stu-id="d52b8-107">The following example shows how to include SYSMON in an HTML document.</span></span> <span data-ttu-id="d52b8-108">O exemplo usa o VBScript para adicionar contadores cujos valores são recuperados do computador local, modifica algumas das propriedades SYSMON que controlam como o monitor é exibido e processa o evento OnCounterAdd.</span><span class="sxs-lookup"><span data-stu-id="d52b8-108">The example uses VBScript to add counters whose values are retrieved from the local computer, modifies some of the SYSMON properties that control how the monitor is displayed, and processes the OnCounterAdd event.</span></span> <span data-ttu-id="d52b8-109">O exemplo usa o caractere curinga ( \* ) para adicionar todas as instâncias do contador de processo.</span><span class="sxs-lookup"><span data-stu-id="d52b8-109">The example uses the wildcard character (\*) to add all instances of the process counter.</span></span>

``` syntax
<HTML>
<BODY BGCOLOR=#C0C0C0>

<SCRIPT LANGUAGE="VBScript">
  Sub Monitor_OnCounterAdded(index)
    Monitor.Counters.Item(1).Width = 8
  End Sub
</Script>
<OBJECT
  CLASSID="clsid:C4D2D8E0-D1DD-11CE-940F-008029004347"
  ID="Monitor"
  HEIGHT=80%
  WIDTH=100%>
</OBJECT>

<SCRIPT LANGUAGE="VBScript">
  Sub Window_OnLoad
    On Error Resume Next
    Monitor.ShowValueBar = False
    Monitor.ShowHorizontalGrid = True
    Monitor.Counters.Add("\Process(*)\% Processor Time")
    Monitor.DisplayType=sysmonLineGraph
    Monitor.GraphTitle="System Performance Overview"
  End Sub
</SCRIPT>

</BODY>
</HTML>
```

 

 




