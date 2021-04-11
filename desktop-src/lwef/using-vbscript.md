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
# <a name="using-vbscript"></a>Usando o VBScript

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O VBScript é uma linguagem de programação incluída no Microsoft Internet Explorer. Para outros navegadores, entre em contato com seu fornecedor sobre o suporte. O VBScript 2,0 (ou posterior) é recomendado para uso com o Agent. Embora as versões anteriores do VBScript possam funcionar com o Agent, elas não têm determinadas funções que talvez você queira usar. Você pode baixar o VBScript 2,0 e obter mais informações sobre o VBScript no site de downloads da Microsoft e no site do Microsoft VBScript.

Para programar o Microsoft Agent do VBScript, use o HTML <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Para eventos, inclua o nome do controle seguido pelo nome do evento e quaisquer parâmetros:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

Você também pode especificar um manipulador de eventos usando o <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Embora o Microsoft Internet Explorer ofereça suporte a essa última sintaxe, nem todos os navegadores fazem. Para compatibilidade, use apenas a sintaxe anterior para eventos.

Com o VBScript (2,0 ou posterior), você pode verificar se o Microsoft Agent está instalado tentando criar o objeto e verificando se ele existe. O exemplo a seguir demonstra como verificar o controle do agente sem disparar um download automático do controle (como aconteceria se você incluísse uma <OBJECT> marca para o controle na página):

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

 

 




