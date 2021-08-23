---
title: Evento DragComplete
description: Evento DragComplete
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ec931a8d5f303dbc1eff5c2f97c018486c4b2fa7326de3e70fbf47a949aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976666"
---
# <a name="dragcomplete-event"></a>Evento DragComplete

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o usuário termina de arrastar um caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent * * * \_ DragComplete* *  **(ByVal** *caractereid*,  *botão* ByVal, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere arrastado como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botão*      | Retorna um inteiro que identifica o botão que foi pressionado e liberado para causar o evento. O argumento do botão é um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits é definido, indicando o botão que causou o evento.                                                                                                                                                                                                                                                                                |
| *Alternância*       | Retorna um inteiro que corresponde ao estado das teclas SHIFT, CTRL e ALT quando o botão especificado no argumento Button é pressionado ou liberado. Um bit será definido se a chave estiver inoperante. O argumento Shift é um campo de campo com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento Shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas. Por exemplo, se CTRL e ALT forem pressionadas, o valor de Shift seria 6. |
| *X, Y*         | Retorna um inteiro que especifica o local atual do ponteiro do mouse. Os valores X e Y são sempre expressos em pixels, em relação ao canto superior esquerdo da tela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado somente para o cliente de entrada-ativo de um caractere. Quando o usuário arrasta um caractere sem entrada-cliente ativo, o servidor define seu último cliente de entrada-ativo como o cliente de entrada-ativo atual, enviando o evento [**ActivateInput**](activateinput-event.md) para esse cliente e, em seguida, enviando os eventos [**DragStart**](dragstart-event.md) e **DragComplete** .

### <a name="see-also"></a>Consulte Também

[**Evento DragStart**](dragstart-event.md)


 

 




