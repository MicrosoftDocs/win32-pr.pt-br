---
title: Trabalhando com paletas
description: Trabalhando com paletas
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- WM_CAP_PAL_PASTE mensagem
- macro capPalettePaste
- WM_CAP_PAL_OPEN mensagem
- macro capPaletteOpen
- WM_CAP_PAL_AUTOCREATE mensagem
- macro capPaletteAuto
- WM_CAP_PAL_MANUALCREATE mensagem
- macro capPaletteManual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51f9399520b5a3cefc046959c0d59d7abe9d0f1b6ab19662f750720afd16447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686706"
---
# <a name="working-with-palettes"></a>Trabalhando com paletas

Inicialmente, se o formato de captura de vídeo exigir uma paleta, a janela de captura usará a paleta fornecida pelo driver de captura. Essa paleta pode consistir em valores de escala de cinza para reprodução em preto e branco ou uma ampla seleção de valores de cores. Você pode recuperar uma paleta existente para substituir a paleta padrão usando a mensagem [**WM \_ CAP PAL \_ \_ PASTE**](wm-cap-pal-paste.md) ou [**WM CAP PAL \_ \_ \_ OPEN**](wm-cap-pal-open.md) (ou a [**macro capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) ou [**capPaletteOpen).**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) Como alternativa, você pode criar uma paleta personalizada para substituir a paleta padrão usando a mensagem [**WM \_ CAP PAL \_ \_ AUTOCREATE**](wm-cap-pal-autocreate.md) ou [**WM CAP PAL \_ \_ \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) (ou a [**macro capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) ou [**capPaletteManual).**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) Depois de substituir a paleta padrão, a janela de captura e o driver usam a paleta de substituição até que você crie ou abra outra paleta.

A mensagem WM \_ CAP \_ PAL \_ AUTOCREATE ou WM \_ CAP PAL \_ MANUALCREATE \_ cria uma paleta otimizada com base na entrada de vídeo atual. Essa paleta personalizada oferece a melhor fidelidade de cores a uma sequência de vídeo, pois ela se baseia nas cores existentes na sequência. A janela de captura cria um histograma tridimensional das cores que ela amostra. Ele reduz o número de cores examinando o erro absoluto entre cores adjacentes e consolidando-as com o menor valor de erro.

Ao enviar WM \_ CAP PAL AUTOCREATE, você deve especificar o número de quadros para o AVICap a ser amostrado e especificar o tamanho da \_ \_ paleta de cores. Ao especificar o número de quadros, inclua quadros suficientes para garantir que todas as cores na sequência sejam amostradas.

Você pode experimentar o quadro atual usando WM \_ CAP \_ PAL \_ MANUALCREATE. Usando essa mensagem com vários quadros selecionados manualmente, você pode criar uma paleta que contém as cores que você deseja que apareçam na paleta.

Uma paleta pode conter até 256 cores. Se você mesclar paletas ou se a sequência de vídeo for exibida simultaneamente com outros vídeos ou imagens, deverá usar uma seleção de cores menor para que as cores de cada imagem ou clipe de vídeo possam coexistir.

Salve uma nova paleta usando a mensagem [**WM \_ CAP PAL \_ \_ SAVE**](wm-cap-pal-save.md) (ou a macro [**capPaletteSave)**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) e recupere-a posteriormente usando a mensagem [**WM CAP PAL \_ \_ \_ OPEN.**](wm-cap-pal-open.md) Você pode salvar uma paleta para pós-processamento da paleta ou para uso em outro aplicativo.

Você pode colar uma paleta da área de transferência na janela de captura usando a mensagem [**WM \_ CAP PAL \_ \_ PASTE.**](wm-cap-pal-paste.md) A janela de captura passa a paleta para o driver de captura. Outros aplicativos podem copiar paletas para a área de transferência. Você também pode copiar uma paleta para a área de transferência usando a mensagem [**WM \_ CAP EDIT \_ \_ COPY**](wm-cap-edit-copy.md) (ou a [**macro capEditCopy).**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) Essa mensagem copia o buffer do quadro de vídeo, incluindo a paleta, para a área de transferência.

 

 




