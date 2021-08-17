---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835ffc22e23643d306b361977a4bbe8b04e6481f8a577c3c2cef959b4be46ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963086"
---
# <a name="dragstart-event"></a>Evento DragStart

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando o usuário começa a arrastar um caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agent*** \_ DragStart* *  **(ByVal** *CharacterID*, **(botão ByVal** , **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y***)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere clicado como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botão*      | Retorna um inteiro que identifica o botão que foi pressionado e liberado para causar o evento. O argumento do botão é um campo de bits com bits correspondentes ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão central (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits está definido, indicando o botão que causou o evento.                                                                                                                                                                                                                                                                                |
| *Shift*       | Retorna um inteiro que corresponde ao estado das teclas SHIFT, CTRL e ALT quando o botão especificado no argumento de botão é pressionado ou liberado. Um bit será definido se a chave estiver inobada. O argumento shift é um campo de bits com os bits menos significativos correspondentes à tecla SHIFT (bit 0), à tecla CTRL (bit 1) e à tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas. Por exemplo, se CTRL e ALT fossem pressionados, o valor de shift seria 6. |
| *X, Y*         | Retorna um inteiro que especifica o local atual do ponteiro do mouse. Os valores X e Y são sempre expressos em pixels, em relação ao canto superior esquerdo da tela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado somente para o cliente ativo de entrada de um caractere. Quando o usuário arrasta um caractere sem cliente ativo de entrada, o servidor define seu último cliente ativo de entrada como o cliente atual de entrada ativa, enviando o evento [**ActivateInput**](activateinput-event.md) para esse cliente e, em seguida, enviando o **evento DragStart.**

### <a name="see-also"></a>Consulte Também

[**Evento DragComplete**](dragcomplete-event.md)


 

 




