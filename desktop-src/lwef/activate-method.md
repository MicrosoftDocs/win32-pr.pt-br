---
title: Método Activate
description: Método Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5032c7c7f2faf7ec53028a0cc0ce55847fe300864bb531968fc8190b4e00d164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753155"
---
# <a name="activate-method"></a>Método Activate

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Descrição**](../wmformat/description.md)
</dt> <dd>

Define o cliente ou caractere ativo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Ativar_ *  \[ *Estado*\]



| Parte    | Descrição                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Opcional. Você pode especificar os seguintes valores para esse parâmetro: 0 Não o cliente ativo.<br/> 1 O cliente ativo. <br/> 2 (Padrão) O caractere mais alto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando vários caracteres estão visíveis, apenas um dos caracteres recebe entrada de fala por vez. Da mesma forma, quando vários aplicativos cliente compartilham o mesmo caractere, somente um dos clientes recebe entrada do mouse (por exemplo, eventos de clique ou arrastar do controle do Microsoft Agent). O conjunto de caracteres para receber o mouse e a entrada de fala é o caractere mais alto e o cliente que recebe a entrada é o cliente ativo desse caractere. (A janela do caractere superior também aparece na parte superior da ordem z da janela de caracteres.) Normalmente, o usuário determina o caractere mais alto selecionando explicitamente o caractere. No entanto, a ativação mais alta também muda quando um caractere é mostrado ou oculto (o caractere se torna ou não é mais superior, respectivamente.)

Você também pode usar esse método para gerenciar explicitamente quando o cliente recebe entradas direcionadas para o caractere, como quando o próprio aplicativo se torna ativo. Por exemplo, definir *Estado* como 2 torna o caractere mais alto e o cliente recebe todos os eventos de entrada de mouse e fala gerados da interação do usuário com o caractere. Portanto, ele também torna seu cliente o cliente ativo de entrada do caractere.

No entanto, você também pode definir a si mesmo como o cliente ativo para um caractere sem tornar o caractere mais alto, definindo *Estado* como 1. Isso permite que o cliente receba uma entrada direcionada para esse caractere quando o caractere se torna mais alto. Da mesma forma, você pode definir seu cliente como não o cliente ativo (não para receber entrada) quando o caractere se torna mais alto, definindo *Estado* como 0.

Evite chamar esse método diretamente após um [**método**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) Show. **Mostrar** define automaticamente o cliente ativo de entrada. Quando o caractere estiver oculto, [**a chamada Ativar**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) poderá falhar se for processada antes que o método **Show** seja concluído.

Se você chamar esse método para uma função, ele retornará um valor booliana que indica se o método foi bem-sucedido. A tentativa de chamar esse método com *o parâmetro State* definido como 2 quando o caractere especificado estiver oculto falhará. Da mesma forma, se você definir *Estado* como 0 e seu aplicativo for o único cliente, essa chamada falhará porque um caractere sempre deverá ter um cliente mais alto.


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
> Chamar esse método com *Estado* definido como 1 normalmente não gera um evento [**ActivateInput,**](https://www.bing.com/search?q=**ActivateInput**) a menos que não haja outros caracteres carregados ou seu aplicativo já esteja ativo de entrada.

 

## <a name="see-also"></a>Consulte Também

[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)


 

