---
title: Método de interrupção
description: Método de interrupção
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366020"
---
# <a name="interrupt-method"></a>Método de interrupção

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Interrompe a animação para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *").* *  *Solicitação* de interrupção



| Parte      | Descrição                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Solicitação* | Um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) para uma chamada de animação específica. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar isso para sincronizar a animação entre os caracteres. Por exemplo, se outro caractere estiver em uma animação de looping, esse método irá parar o loop e passar para a próxima animação na fila do caractere. Não é possível interromper uma animação de caracteres que você não está usando (que você não carregou).

Para especificar o parâmetro de solicitação, você deve criar uma variável e atribuir a solicitação de animação que deseja interromper:


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



Não é possível interromper a animação do mesmo caractere que você especifica nesse método, pois o servidor enfileira o método de **interrupção** na fila de animação desse caractere. Portanto, você só pode usar a **interrupção** para interromper a animação de outro caractere que você carregou.

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .

> [!Note]  
> A **interrupção** não libera a fila do caractere; Ele interrompe a animação existente e passa para a próxima animação na fila do caractere. Para interromper e liberar a fila de um caractere, use o método [**Stop**](stop-method.md) .

 

## <a name="see-also"></a>Consulte Também

[**Método Stop**](stop-method.md)


 

 