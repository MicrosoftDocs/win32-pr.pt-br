---
title: método Stop (recursos de ambiente de Windows herdados)
description: Método Stop
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572a93db5697aaae0dcfed6b45a834323c106bba447d2d9a8e94109f788af25c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745958"
---
# <a name="stop-method-legacy-windows-environment-features"></a>método Stop (recursos de ambiente de Windows herdados)

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Interrompe a animação para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). Parar_ *  \[ *solicitação*\]



| Parte      | Descrição                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Solicitação* | Opcional. Um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) que especifica uma chamada de animação específica. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Para especificar o parâmetro de solicitação, você deve criar uma variável e atribuir a solicitação de animação que deseja parar. Se você não definir o parâmetro de **solicitação** , o servidor interromperá todas as animações para o caractere, incluindo chamadas [**Get**](get-method.md) em fila e desmarcará sua fila de animação, a menos que o caractere esteja atualmente reproduzindo sua animação de **ocultação** ou **exibição** . Esse método não interrompe chamadas **Get** não enfileiradas.

Para interromper uma animação específica ou [**obter**](get-method.md) uma chamada, declare uma variável de objeto e atribua sua solicitação de animação a essa variável:


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



Esse método não gerará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Consulte Também

[**Método do opAll**](stopall-method.md)


 

 
