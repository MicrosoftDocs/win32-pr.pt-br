---
title: Manipuladores de eventos de ambiente
description: Manipuladores de eventos de ambiente
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Capas do Windows Media Player, manipuladores de eventos de ambiente
- capas, manipuladores de eventos de ambiente
- referência para capas, manipuladores de eventos de ambiente
- manipuladores de eventos de ambiente
- eventos, ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363777"
---
# <a name="ambient-event-handlers"></a>Manipuladores de eventos de ambiente

Os manipuladores de eventos a seguir podem ser implementados para a maioria dos elementos de capa. Os atributos de evento de ambiente acessados com a palavra-chave do **evento** podem ser usados dentro de um manipulador de eventos para determinar o estado do teclado e do mouse no momento do evento.



| Manipulador de eventos                                   | Descrição                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*atributo* \_ OnChange](attribute-onchange.md) | Quando um atributo de aparência muda de valor, ocorre um evento que pode ser manipulado por um manipulador de eventos. O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e "OnChange", como "valor \_ onChange". |
| [desfoque](onblur.md)                            | Manipula um evento que ocorre quando o elemento perde o foco do teclado.                                                                                                                                                       |
| [OnClick](onclick.md)                          | Manipula um evento que ocorre quando o usuário clica no elemento.                                                                                                                                                                |
| [AoClicarDuasVezes](ondblclick.md)                    | Manipula um evento que ocorre quando o usuário clica duas vezes no elemento.                                                                                                                                                         |
| [onendalphablend](onendalphablend.md)          | Manipula um evento que ocorre quando um elemento conclui uma operação **alphaBlendTo** .                                                                                                                                         |
| [onendmove](onendmove.md)                      | Manipula um evento que ocorre quando um elemento conclui uma operação **MoveTo** .                                                                                                                                                |
| [enfoco](onfocus.md)                          | Manipula um evento que ocorre quando o elemento recebe o foco do teclado.                                                                                                                                                    |
| [AoApertarTecla](onkeydown.md)                      | Manipula um evento que ocorre quando uma tecla é pressionada.                                                                                                                                                                           |
| [OnKeyPress](onkeypress.md)                    | Manipula um evento que ocorre quando o usuário pressiona uma tecla alfanumérica.                                                                                                                                                       |
| [OnKeyUp](onkeyup.md)                          | Manipula um evento que ocorre quando uma chave é liberada.                                                                                                                                                                          |
| [OnMouseDown](onmousedown.md)                  | Manipula um evento que ocorre quando o usuário clica em um botão do mouse.                                                                                                                                                             |
| [OnMouseMove](onmousemove.md)                  | Manipula um evento que ocorre quando o usuário move o ponteiro do mouse enquanto ele está sobre um elemento.                                                                                                                               |
| [onmouseout](onmouseout.md)                    | Manipula um evento que ocorre quando o usuário move o ponteiro para fora do elemento.                                                                                                                                                 |
| [onmouseover](onmouseover.md)                  | Manipula um evento que ocorre quando o usuário coloca o ponteiro pela primeira vez sobre o elemento.                                                                                                                                         |
| [OnMouseUp](onmouseup.md)                      | Manipula um evento que ocorre quando o usuário libera um botão do mouse enquanto o ponteiro está sobre o elemento.                                                                                                                     |
| [OnResize](onresize.md)                        | Manipula um evento que ocorre quando um controle é redimensionado.                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos de evento de ambiente**](ambient-event-attributes.md)
</dt> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




