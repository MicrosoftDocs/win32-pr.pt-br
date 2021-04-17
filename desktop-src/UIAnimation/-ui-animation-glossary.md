---
title: Glossário de animação do Windows
description: Este glossário contém termos e acrônimos de interesse para os desenvolvedores que usam o Gerenciador de animação do Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Animação das janelas de animação do Windows, Glossário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104498967"
---
# <a name="windows-animation-glossary"></a>Glossário de animação do Windows

Este glossário contém termos e acrônimos de interesse para os desenvolvedores que usam o Gerenciador de animação do Windows.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animação** 
</dt> <dd>

Uma sequência de imagens sintéticas e sucessivas que produz uma ilusão de movimento quando reproduzidas.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Gerenciador de animação** 
</dt> <dd>

Um componente principal da animação do Windows e a interface de programação central para gerenciar (criar, agendar e controlar) animações.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**temporizador de animação**
</dt> <dd>

Um componente para fornecer serviços de tempo que podem ser usados em conjunto com o Gerenciador de animação. Ele acelera dinamicamente a taxa de quadros com base no aplicativo e na carga do sistema ou no modo de baixa energia. Consulte também: limitação.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variável de animação** 
</dt> <dd>

Um valor que pode ser animado. As variáveis de animação podem ser usadas para representar a posição, o tamanho, a rotação, a transparência e outras qualidades dos objetos visíveis.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**cancelamento**
</dt> <dd>

O processo de remover um storyboard do agendamento antes que ele comece a ser reproduzido.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**çã**
</dt> <dd>

Uma distorção da percepção de tempo de um Storyboard. O sistema aumenta a taxa em que o storyboard progride passando valores de tempo de entrada que aumentam mais rápido do que o relógio do sistema.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**final**
</dt> <dd>

O processo de direcionar um Storyboard para sair de qualquer loop indefinido. Se o loop tiver começado, a iteração atual será concluída e o restante do storyboard será tocado. Caso contrário, a parte em loop do storyboard será ignorada inteiramente.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**quadro** 
</dt> <dd>

Uma única imagem em um filme ou em uma animação.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**taxa de quadros** 
</dt> <dd>

O número de quadros exibidos por segundo. Taxas de quadros mais altas geralmente produzem movimento mais suave na imagem.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolador**
</dt> <dd>

O objeto de programação que faz a interpolação matemática do valor e a velocidade de uma variável para uma transição.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**Keyframe**
</dt> <dd>

Um momento no tempo dentro de um storyboard, que pode ser especificado em relação ao início do storyboard, em relação a outro quadro-chave, ou na hora de término de uma transição e usado para especificar a hora de início e de término de outras transições ou um ciclo dentro do storyboard.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**While**
</dt> <dd>

Uma seção de um storyboard entre dois quadros-chave que é reproduzido repetidamente. Um loop pode reproduzir um número finito de vezes ou indefinidamente.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**comparação de prioridade** 
</dt> <dd>

Código definido pelo cliente que compara dois storyboards, um já agendado e o outro a ser agendado, para determinar sua prioridade relativa. Um storyboard agendado pode ser cortado, compactado, cancelado ou concluído para habilitar o agendamento do storyboard com prioridade mais alta.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**storyboard** 
</dt> <dd>

Um grupo de transições de animação sincronizadas em relação umas às outras.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**marca** de 
</dt> <dd>

Um par que consiste em uma ID de inteiro e um objeto COM usado por um aplicativo para identificar as variáveis de animação e os storyboards dentro do escopo de um Gerenciador de animação específico.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitação** 
</dt> <dd>

Ajuste dinâmico da taxa de quadros de uma animação para atender a determinados requisitos. A limitação ajuda a garantir que as animações sejam renderizadas em uma taxa de quadros consistente, minimizando o uso de recursos do sistema para renderização a uma taxa que está além do que é necessário ou útil.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**escala** 
</dt> <dd>

Um evento de temporizador que normalmente dispara a renderização de um único quadro.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transição** 
</dt> <dd>

Um constructo que define atualizações progressivas para uma variável de animação em um período de tempo.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**restrições**
</dt> <dd>

Preempção do controle de um storyboard de uma variável de animação com um storyboard de prioridade mais alta. Se o corte de um storyboard em uma ou mais variáveis fizer com que o storyboard termine prematuramente, ele será considerado truncado. Consulte também: truncamento.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**truncamento**
</dt> <dd>

Terminar um storyboard prematuramente ao apropriar o controle de uma ou mais das variáveis que ele anima com um ou mais storyboards de prioridade mais alta. Consulte também: corte.

</dd> </dl>

 

 




