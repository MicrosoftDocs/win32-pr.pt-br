---
title: Evento Clicar
description: Evento Clicar
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3956d19e833a3e0a5f71192b2846ef9cb270ad10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364271"
---
# <a name="click-event"></a>Evento Clicar

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o usuário clica em um caractere ou no ícone do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

 *Subagent * * * \_ clique* *  **(ByVal** *caractereid*,  *botão* ByVal, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere clicado como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botão*      | Retorna um inteiro que identifica o botão que foi pressionado e liberado para causar o evento. O argumento do botão é um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits é definido, indicando o botão que causou o evento. Se o caractere incluir um ícone da barra de tarefas e o bit 13 também for definido, o clique ocorrerá no ícone da barra de tarefas.                                                                                                                                                                      |
| *Alternância*       | Retorna um inteiro que corresponde ao estado das teclas SHIFT, CTRL e ALT quando o botão especificado no argumento Button é pressionado ou liberado. Um bit será definido se a chave estiver inoperante. O argumento Shift é um campo de campo com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento Shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas. Por exemplo, se CTRL e ALT forem pressionadas, o valor de Shift seria 6. |
| *X, Y*         | Retorna um inteiro que especifica o local atual do ponteiro do mouse. Os valores X e Y são sempre expressos em pixels, em relação ao canto superior esquerdo da tela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado somente para o cliente de entrada-ativo de um caractere. Quando o usuário clica em um caractere ou em seu ícone da barra de tarefas sem entrada – cliente ativo, o servidor envia o evento para o cliente ativo. Se o caractere estiver visível ([**visível**](visible-property.md)  =  **true**), a ação do usuário também definirá o último cliente de entrada-ativo do caractere como o cliente de entrada-ativo atual, enviando o evento [**ActivateInput**](activateinput-event.md) para esse cliente e, em seguida, enviando o evento de **clique** . Se o caractere estiver oculto (**visível**  =  **false**) e o usuário clicar no ícone da barra de tarefas do caractere usando o botão 1, o caractere também será exibido automaticamente.

> [!Note]  
> Clicar em um caractere não desabilita todas as outras saídas de caractere (todos os caracteres). No entanto, pressionar a tecla de escuta libera a saída do caractere de entrada-ativo e dispara o evento [**RequestComplete**](requestcomplete-event.md) , passando uma [solicitação. status](status-property.md) que indica que a fila do cliente foi interrompida.

 

 

 




