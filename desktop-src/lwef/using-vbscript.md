---
title: Usando o VBScript
description: Usando o VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691ed6bf520c83e4b679bb174274abb984eaa2f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159941"
---
# <a name="using-vbscript"></a><span data-ttu-id="d0f0e-103">Usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="d0f0e-103">Using VBScript</span></span>

<span data-ttu-id="d0f0e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0f0e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d0f0e-105">O VBScript é uma linguagem de programação incluída no Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-105">VBScript is a programming language included with Microsoft Internet Explorer.</span></span> <span data-ttu-id="d0f0e-106">Para outros navegadores, entre em contato com seu fornecedor sobre o suporte.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-106">For other browsers, contact your vendor about support.</span></span> <span data-ttu-id="d0f0e-107">O VBScript 2,0 (ou posterior) é recomendado para uso com o Agent.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-107">VBScript 2.0 (or later) is recommended for use with Agent.</span></span> <span data-ttu-id="d0f0e-108">Embora as versões anteriores do VBScript possam funcionar com o Agent, elas não têm determinadas funções que talvez você queira usar.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-108">Although earlier versions of VBScript may work with Agent, they lack certain functions that you may want to use.</span></span> <span data-ttu-id="d0f0e-109">Você pode baixar o VBScript 2,0 e obter mais informações sobre o VBScript no site de downloads da Microsoft e no site do Microsoft VBScript.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-109">You can download VBScript 2.0 and obtain further information on VBScript at the Microsoft Downloads site and the Microsoft VBScript site.</span></span>

<span data-ttu-id="d0f0e-110">Para programar o Microsoft Agent do VBScript, use o HTML</span><span class="sxs-lookup"><span data-stu-id="d0f0e-110">To program Microsoft Agent from VBScript, use the HTML</span></span> <SCRIPT> <span data-ttu-id="d0f0e-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span><span class="sxs-lookup"><span data-stu-id="d0f0e-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span></span>

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

<span data-ttu-id="d0f0e-112">Para eventos, inclua o nome do controle seguido pelo nome do evento e quaisquer parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d0f0e-112">For events, include the name of the control followed by the name of the event and any parameters:</span></span>

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

<span data-ttu-id="d0f0e-113">Você também pode especificar um manipulador de eventos usando o</span><span class="sxs-lookup"><span data-stu-id="d0f0e-113">You can also specify an event handler using the</span></span> <SCRIPT> <span data-ttu-id="d0f0e-114">tag's **For...Event** syntax:</span><span class="sxs-lookup"><span data-stu-id="d0f0e-114">tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

<span data-ttu-id="d0f0e-115">Embora o Microsoft Internet Explorer ofereça suporte a essa última sintaxe, nem todos os navegadores fazem.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-115">Although Microsoft Internet Explorer supports this latter syntax, not all browsers do.</span></span> <span data-ttu-id="d0f0e-116">Para compatibilidade, use apenas a sintaxe anterior para eventos.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-116">For compatibility, use only the former syntax for events.</span></span>

<span data-ttu-id="d0f0e-117">Com o VBScript (2,0 ou posterior), você pode verificar se o Microsoft Agent está instalado tentando criar o objeto e verificando se ele existe.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-117">With VBScript (2.0 or later), you can verify whether Microsoft Agent is installed by trying to create the object and checking to see if it exists.</span></span> <span data-ttu-id="d0f0e-118">O exemplo a seguir demonstra como verificar o controle do agente sem disparar um download automático do controle (como aconteceria se você incluísse uma <OBJECT> marca para o controle na página):</span><span class="sxs-lookup"><span data-stu-id="d0f0e-118">The following sample demonstrates how to check for the Agent control without triggering an auto-download of the control (as would happen if you included an <OBJECT> tag for the control on the page):</span></span>

``` syntax
<!-- WARNING - This code requires VBScript 2.0.
It will always fail to detect the Agent control
in VbScript 1.x, because CreateObject doesn't work.
-->

<SCRIPT LANGUAGE=VBSCRIPT>
If HaveAgent() Then
      'Microsoft Agent control was found.
document.write "<H2 align=center>Found</H2>"
Else
      'Microsoft Agent control was not found.
document.write "<H2 align=center>Not Found</H2>"
End If

Function HaveAgent()
' This procedure attempts to create an Agent Control object.
' If it succeeds, it returns True.
'    This means the control is available on the client.
' If it fails, it returns False.
'    This means the control hasn't been installed on the client.

   Dim agent
   HaveAgent = False
   On Error Resume Next
   Set agent = CreateObject("Agent.Control.1")
   HaveAgent = IsObject(agent)

End Function

</SCRIPT>
```

 

 




