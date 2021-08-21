---
title: Evento Clicar
description: Evento Clicar
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc10726c91612a6d43c4b7f8ceb0509fc347904f1328c9b99a3ec05d8e2eb0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480182"
---
# <a name="click-event"></a>Evento Clicar

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando o usuário clica em um caractere ou no ícone do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agente*** \_ Clique* *  **(ByVal** *CharacterID,* **Botão ByVal** , **ByVal** *Shift,* **ByVal** *X,* **ByVal** *Y***)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere clicado como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botão*      | Retorna um inteiro que identifica o botão que foi pressionado e liberado para causar o evento. O argumento do botão é um campo de bits com bits correspondentes ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão central (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits está definido, indicando o botão que causou o evento. Se o caractere incluir um ícone de barra de tarefas e o bit 13 também estiver definido, o clique ocorreu no ícone da barra de tarefas.                                                                                                                                                                      |
| *Shift*       | Retorna um inteiro que corresponde ao estado das teclas SHIFT, CTRL e ALT quando o botão especificado no argumento de botão é pressionado ou liberado. Um bit será definido se a chave estiver inobada. O argumento shift é um campo de bits com os bits menos significativos correspondentes à tecla SHIFT (bit 0), à tecla CTRL (bit 1) e à tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas. Por exemplo, se CTRL e ALT fossem pressionados, o valor de shift seria 6. |
| *X, Y*         | Retorna um inteiro que especifica o local atual do ponteiro do mouse. Os valores X e Y são sempre expressos em pixels, em relação ao canto superior esquerdo da tela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado somente para o cliente ativo de entrada de um caractere. Quando o usuário clica em um caractere ou em seu ícone de barra de tarefas sem cliente ativo de entrada, o servidor envia o evento para seu cliente ativo. Se o caractere estiver visível ([**Visível**](visible-property.md)True ), a ação do usuário também define o último cliente ativo de entrada do caractere como o cliente atual de entrada ativa, enviando o evento  =   [**ActivateInput**](activateinput-event.md) para esse cliente e, em seguida, enviando o evento **Click.** Se o caractere estiver oculto (**Visible** False ) e o usuário clicar no ícone da barra de tarefas do caractere usando o botão 1, o caractere também  =  será mostrado automaticamente.

> [!Note]  
> Clicar em um caractere não desabilita todas as outras saídas de caractere (todos os caracteres). No entanto, pressionar a tecla Listening libera a saída do caractere ativo de entrada e dispara o evento [**RequestComplete,**](requestcomplete-event.md) passando um [Request.Status](status-property.md) que indica que a fila do cliente foi interrompida.

 

 

 




