---
title: Windows Glossário de animação
description: Este glossário contém termos e acrônimos de interesse para desenvolvedores usando o Windows Animation Manager.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Windows Animação Windows animação, glossário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb477edcaa49aa8baff1bc628ca5d94c13dacc0e552137275ff1e92d8e4cfae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137389"
---
# <a name="windows-animation-glossary"></a>Windows Glossário de animação

Este glossário contém termos e acrônimos de interesse para desenvolvedores usando o Windows Animation Manager.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animação** 
</dt> <dd>

Uma sequência de imagens ainda sintéticas e sucessivas que produz uma ilusão de movimento quando tocada.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**gerenciador de animação** 
</dt> <dd>

Um componente principal do Windows Animation e a interface programática central para gerenciar (criar, agendar e controlar) animações.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**temporizador de animação**
</dt> <dd>

Um componente para fornecer serviços de tempo que podem ser usados em conjunto com o gerenciador de animação. Ela acelera dinamicamente a taxa de quadros com base na carga do aplicativo e do sistema ou no modo de baixa energia. Consulte também: throttling.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variável de animação** 
</dt> <dd>

Um valor que pode ser animado. As variáveis de animação podem ser usadas para representar a posição, o tamanho, a rotação, a transparência e outras qualidades de objetos visíveis.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**Cancelamento**
</dt> <dd>

O processo de remoção de um storyboard da agenda antes de começar a ser a reprodução.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**Compressão**
</dt> <dd>

Uma distorção da percepção de tempo de um storyboard. O sistema aumenta a taxa na qual o storyboard progride passando valores de tempo de entrada que aumentam mais rapidamente do que o relógio do sistema.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**Conclusão**
</dt> <dd>

O processo de direcionar um storyboard para sair de qualquer loop indefinido. Se o loop tiver começado, a iteração atual será concluída e o restante do storyboard será reproduzir. Caso contrário, a parte em loop do storyboard será ignorada inteiramente.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**quadro** 
</dt> <dd>

Uma única imagem em um filme ou uma animação.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**taxa de quadros** 
</dt> <dd>

O número de quadros exibidos por segundo. Taxas de quadros mais altas geralmente produzem um movimento mais suave na imagem.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolador**
</dt> <dd>

O objeto de programação que faz a interpolação matemática do valor e da velocidade de uma variável para uma transição.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**Keyframe**
</dt> <dd>

Um momento no tempo dentro de um storyboard, que pode ser especificado em relação ao início do storyboard, em relação a outro quadro-chave ou no momento final de uma transição, e usado para especificar a hora de início e término de outras transições ou um ciclo dentro do storyboard.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**Loop**
</dt> <dd>

Uma seção de um storyboard entre dois keyframes que é repetido. Um loop pode reproduzir um número finito de vezes ou indefinidamente.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**comparação de prioridade** 
</dt> <dd>

Código definido pelo cliente que compara dois storyboards, um já agendado e o outro prestes a ser agendado, para determinar sua prioridade relativa. Um storyboard agendado pode ser cortado, compactado, cancelado ou concluído para habilitar o agendamento do storyboard com prioridade mais alta.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**storyboard** 
</dt> <dd>

Um grupo de animação faz a transição sincronizada em relação umas às outras.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**tag** 
</dt> <dd>

Um par que consiste em uma ID de inteiro e um objeto COM usado por um aplicativo para identificar variáveis de animação e storyboards dentro do escopo de um gerenciador de animação específico.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**throttling** 
</dt> <dd>

Ajustar dinamicamente a taxa de quadros de uma animação para atender a determinados requisitos. A throttling ajuda a garantir que as animações sejam renderizadas em uma taxa de quadros consistente, minimizando o uso de recursos do sistema para renderização em uma taxa que está além do que é necessário ou útil.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**tique** 
</dt> <dd>

Um evento de temporizador que normalmente dispara a renderização de um único quadro.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transição** 
</dt> <dd>

Um constructo que define atualizações progressivas para uma variável de animação durante um período de tempo.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**Aparar**
</dt> <dd>

Preempção do controle de um storyboard de uma variável de animação com um storyboard de prioridade mais alta. Se o corte de um storyboard em uma ou mais variáveis faz com que o storyboard termine prematuramente, ele será considerado truncado. Confira também: truncamento.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**Truncamento**
</dt> <dd>

Encerrar um storyboard prematuramente preempção do controle de uma ou mais das variáveis que ele anima com um ou mais storyboards de prioridade mais alta. Confira também: corte.

</dd> </dl>

 

 




