---
description: O sistema mantém um cache de contextos de dispositivo de vídeo que ele usa para contextos de dispositivo comuns, pai e de janela.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Exibir cache de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96bbf8cb388e31e43a0eacf9200b638fe8a232749dd5e2ef8ab67318b30d9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062426"
---
# <a name="display-device-context-cache"></a>Exibir cache de contexto do dispositivo

O sistema mantém um cache de contextos de dispositivo de vídeo que ele usa para contextos de dispositivo comuns, pai e de janela. O sistema recupera um contexto de dispositivo do cache sempre que um aplicativo chama a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ; o sistema retorna o DC ao cache quando o aplicativo chama a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) ou [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) subsequentemente.

Não há um limite predeterminado na quantidade de contextos de dispositivo que um cache pode conter; o sistema cria um novo contexto de dispositivo de vídeo para o cache, se nenhum estiver disponível. Considerando isso, um aplicativo pode ter mais de cinco contextos de dispositivo ativos do cache de cada vez. No entanto, o aplicativo deve continuar a liberar esses contextos de dispositivo após o uso. Como novos contextos de dispositivo de exibição para o cache são alocados no espaço de heap do aplicativo, a falha ao liberar os contextos de dispositivo eventualmente consome todo o espaço de heap disponível. O sistema indica essa falha retornando um erro quando não é possível alocar espaço para o novo contexto do dispositivo. Outras funções não relacionadas ao cache também podem retornar erros.

 

 



