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
ms.openlocfilehash: f09cbbe3ffc8ea21d1ecf8545f036f5ba6dfb927
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105749563"
---
# <a name="working-with-palettes"></a>Trabalhando com paletas

Inicialmente, se o formato de captura de vídeo exigir uma paleta, a janela de captura usará a paleta fornecida pelo driver de captura. Essa paleta pode consistir em valores de escala cinza para reprodução em preto e branco, ou uma ampla seleção de valores de cor. Você pode recuperar uma paleta existente para substituir a paleta padrão usando a mensagem [**do WM \_ Cap \_ PAL \_ Paste**](wm-cap-pal-paste.md) ou [**WM Cap da \_ \_ PAL \_ aberta**](wm-cap-pal-open.md) (ou a macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) ou [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) ). Como alternativa, você pode criar uma paleta personalizada para substituir a paleta padrão usando a mensagem [**do WM \_ Cap \_ PAL \_ Autocreate**](wm-cap-pal-autocreate.md) ou [**WM \_ Cap \_ endpal \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) (ou a macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) ou [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) ). Depois de substituir a paleta padrão, a janela de captura e o driver usam a paleta de substituição até que você crie ou abra outra paleta.

A mensagem do WM \_ Cap \_ PAL \_ Autocreate ou WM \_ Cap \_ PAL \_ MANUALCREATE cria uma paleta otimizada com base na entrada de vídeo atual. Essa paleta personalizada fornece uma sequência de vídeo com a melhor fidelidade de cor porque ela se baseia em cores que existem na sequência. A janela de captura cria um histograma tridimensional das cores que ele obtém. Ele reduz o número de cores examinando o erro absoluto entre as cores adjacentes e consolidando-as com o menor valor de erro.

Ao enviar a criação automática do WM \_ Cap \_ PAL \_ , você deve especificar o número de quadros para AVICap a serem amostrados e especificar o tamanho da paleta de cores. Ao especificar o número de quadros, inclua quadros suficientes para garantir que todas as cores na sequência sejam amostradas.

Você pode obter uma amostra do quadro atual usando o WM \_ Cap \_ PAL \_ MANUALCREATE. Usando essa mensagem com vários quadros selecionados manualmente, você pode criar uma paleta que contém as cores que você deseja que apareçam na paleta.

Uma paleta pode conter até 256 cores. Se você mesclar paletas ou se a sequência de vídeo for ser exibida simultaneamente com outro vídeo ou imagens, você deverá usar uma seleção de cor menor para que as cores de cada imagem ou clipe de vídeo possam coexistir.

Você salva uma nova paleta usando a mensagem [**de \_ \_ \_ salvamento do PAL Cap do WM**](wm-cap-pal-save.md) (ou a macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) ) e a recupera posteriormente usando a mensagem de [**\_ \_ \_ abertura da PAL do WM Cap**](wm-cap-pal-open.md) . Você pode salvar uma paleta para pós-processamento da paleta ou para uso em outro aplicativo.

Você pode colar uma paleta da área de transferência na janela de captura usando a mensagem de [**\_ \_ \_ colagem da PAL Cap do WM**](wm-cap-pal-paste.md) . A janela de captura passa a paleta para o driver de captura. Outros aplicativos podem copiar paletas para a área de transferência. Você também pode copiar uma paleta para a área de transferência usando a mensagem de cópia de edição da Cap do WM (ou a macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). [**\_ \_ \_**](wm-cap-edit-copy.md) Esta mensagem copia o buffer de quadros de vídeo, incluindo a paleta, para a área de transferência.

 

 




