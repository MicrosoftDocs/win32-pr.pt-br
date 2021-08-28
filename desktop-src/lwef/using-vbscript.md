---
title: Usando o VBScript
description: Usando o VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bc64419af4d8dc47de5a2393fcf5cb259374ed
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881020"
---
# <a name="using-vbscript"></a>Usando o VBScript

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O VBScript é uma linguagem de programação incluída no Microsoft Internet Explorer. Para outros navegadores, entre em contato com seu fornecedor sobre o suporte. O VBScript 2,0 (ou posterior) é recomendado para uso com o Agent. Embora as versões anteriores do VBScript possam funcionar com o Agent, elas não têm determinadas funções que talvez você queira usar. Você pode baixar o VBScript 2,0 e obter mais informações sobre o VBScript no site de downloads da Microsoft e no site do Microsoft VBScript.

Para programar o Microsoft Agent do VBScript, use as &lt; marcas de script HTML &gt; . Para acessar a interface de programação, use o nome do controle que você atribui &lt; na &gt; marca Object, seguido pelo subobjeto (se houver), o nome do método ou da propriedade e quaisquer parâmetros ou valores com suporte no método ou na propriedade:

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

Você também pode especificar um manipulador de eventos usando &lt; a &gt; marca de script **para...** Sintaxe do evento:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Embora o Microsoft Internet Explorer ofereça suporte a essa última sintaxe, nem todos os navegadores fazem. Para compatibilidade, use apenas a sintaxe anterior para eventos.

Com o VBScript (2,0 ou posterior), você pode verificar se o Microsoft Agent está instalado tentando criar o objeto e verificando se ele existe. O exemplo a seguir demonstra como verificar o controle do agente sem disparar um download automático do controle (como aconteceria se você incluísse uma &lt; &gt; marca de objeto para o controle na página):

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

 

 




