---
title: Método Activate
description: Método Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105796065"
---
# <a name="activate-method"></a>Método Activate

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Ndescrição**](../wmformat/description.md)
</dt> <dd>

Define o caractere ou o cliente ativo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Ativar* *  \[ *estado*\]



| Parte    | Descrição                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Opcional. Você pode especificar os seguintes valores para este parâmetro: 0 não é o cliente ativo.<br/> 1 o cliente ativo. <br/> 2 (padrão) o caractere superior.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando vários caracteres são visíveis, apenas um dos caracteres recebe a entrada de fala de cada vez. Da mesma forma, quando vários aplicativos cliente compartilham o mesmo caractere, apenas um dos clientes recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos). O conjunto de caracteres para receber o mouse e a entrada de fala é o caractere superior e o cliente que recebe a entrada é o cliente ativo desse caractere. (A janela do caractere superior também aparece na parte superior da ordem z da janela de caractere.) Normalmente, o usuário determina o caractere superior selecionando explicitamente o caractere. No entanto, a ativação na extremidade superior também é alterada quando um caractere é mostrado ou oculto (o caractere se torna ou não é mais o mais alto, respectivamente.)

Você também pode usar esse método para gerenciar explicitamente quando o cliente recebe a entrada direcionada para o caractere, como quando o próprio aplicativo se torna ativo. Por exemplo, definir *State* como 2 torna o caractere mais alto e o cliente recebe todos os eventos de entrada de mouse e fala gerados da interação do usuário com o caractere. Portanto, ele também torna o cliente o cliente de entrada-ativo do caractere.

No entanto, você também pode definir a si mesmo como o cliente ativo para um caractere sem tornar o caractere mais alto, definindo o *estado* como 1. Isso permite que o cliente receba entrada direcionada para esse caractere quando o caractere se tornar mais alto. Da mesma forma, você pode definir que o cliente não seja o cliente ativo (não para receber a entrada) quando o caractere se tornar mais alto, definindo *State* como 0.

Evite chamar esse método diretamente após um método [**show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) . **Mostrar** define automaticamente o cliente de entrada-ativo. Quando o caractere estiver oculto, a chamada de [**ativação**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) poderá falhar se for processada antes de o método **show** ser concluído.

Se você chamar esse método para uma função, ele retornará um valor booliano que indica se o método foi bem-sucedido. A tentativa de chamar esse método com o parâmetro de *estado* definido como 2 quando o caractere especificado for oculta falhará. Da mesma forma, se você definir o *estado* como 0 e seu aplicativo for o único cliente, essa chamada falhará porque um caractere sempre deve ter um cliente de nível superior.


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> Chamar esse método com o *estado* definido como 1 normalmente não gera um evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) , a menos que não haja nenhum outro caractere carregado ou seu aplicativo já está em entrada-ativo.

 

## <a name="see-also"></a>Consulte Também

[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)


 

