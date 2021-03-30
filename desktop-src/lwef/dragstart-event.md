---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e382e77c87848226568755c06d2541ebb4db14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005495"
---
# <a name="dragstart-event"></a>Evento DragStart

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o usuário começa a arrastar um caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent * * * \_ DragStart* *  **(ByVal** *characterid*, **(** *botão* ByVal, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere clicado como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botão*      | Retorna um inteiro que identifica o botão que foi pressionado e liberado para causar o evento. O argumento do botão é um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits é definido, indicando o botão que causou o evento.                                                                                                                                                                                                                                                                                |
| *Alternância*       | Retorna um inteiro que corresponde ao estado das teclas SHIFT, CTRL e ALT quando o botão especificado no argumento Button é pressionado ou liberado. Um bit será definido se a chave estiver inoperante. O argumento Shift é um campo de campo com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento Shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas. Por exemplo, se CTRL e ALT forem pressionadas, o valor de Shift seria 6. |
| *X, Y*         | Retorna um inteiro que especifica o local atual do ponteiro do mouse. Os valores X e Y são sempre expressos em pixels, em relação ao canto superior esquerdo da tela.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado somente para o cliente de entrada-ativo de um caractere. Quando o usuário arrasta um caractere sem entrada-cliente ativo, o servidor define seu último cliente de entrada-ativo como o cliente de entrada-ativo atual, enviando o evento [**ActivateInput**](activateinput-event.md) para esse cliente e, em seguida, enviando o evento **DragStart** .

### <a name="see-also"></a>Consulte Também

[**Evento DragComplete**](dragcomplete-event.md)


 

 




