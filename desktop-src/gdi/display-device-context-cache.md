---
description: O sistema mantém um cache de contextos de dispositivo de vídeo que ele usa para contextos de dispositivo comuns, pai e de janela.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Exibir cache de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988834"
---
# <a name="display-device-context-cache"></a>Exibir cache de contexto do dispositivo

O sistema mantém um cache de contextos de dispositivo de vídeo que ele usa para contextos de dispositivo comuns, pai e de janela. O sistema recupera um contexto de dispositivo do cache sempre que um aplicativo chama a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ; o sistema retorna o DC ao cache quando o aplicativo chama a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) ou [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) subsequentemente.

Não há um limite predeterminado na quantidade de contextos de dispositivo que um cache pode conter; o sistema cria um novo contexto de dispositivo de vídeo para o cache, se nenhum estiver disponível. Considerando isso, um aplicativo pode ter mais de cinco contextos de dispositivo ativos do cache de cada vez. No entanto, o aplicativo deve continuar a liberar esses contextos de dispositivo após o uso. Como novos contextos de dispositivo de exibição para o cache são alocados no espaço de heap do aplicativo, a falha ao liberar os contextos de dispositivo eventualmente consome todo o espaço de heap disponível. O sistema indica essa falha retornando um erro quando não é possível alocar espaço para o novo contexto do dispositivo. Outras funções não relacionadas ao cache também podem retornar erros.

 

 



