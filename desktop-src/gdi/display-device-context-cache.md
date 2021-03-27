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
# <a name="display-device-context-cache"></a><span data-ttu-id="839cc-103">Exibir cache de contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="839cc-103">Display Device Context Cache</span></span>

<span data-ttu-id="839cc-104">O sistema mantém um cache de contextos de dispositivo de vídeo que ele usa para contextos de dispositivo comuns, pai e de janela.</span><span class="sxs-lookup"><span data-stu-id="839cc-104">The system maintains a cache of display device contexts that it uses for common, parent, and window device contexts.</span></span> <span data-ttu-id="839cc-105">O sistema recupera um contexto de dispositivo do cache sempre que um aplicativo chama a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ; o sistema retorna o DC ao cache quando o aplicativo chama a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) ou [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="839cc-105">The system retrieves a device context from the cache whenever an application calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function; the system returns the DC to the cache when the application subsequently calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) or [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) function.</span></span>

<span data-ttu-id="839cc-106">Não há um limite predeterminado na quantidade de contextos de dispositivo que um cache pode conter; o sistema cria um novo contexto de dispositivo de vídeo para o cache, se nenhum estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="839cc-106">There is no predetermined limit on the amount of device contexts that a cache can hold; the system creates a new display device context for the cache if none is available.</span></span> <span data-ttu-id="839cc-107">Considerando isso, um aplicativo pode ter mais de cinco contextos de dispositivo ativos do cache de cada vez.</span><span class="sxs-lookup"><span data-stu-id="839cc-107">Given this, an application can have more than five active device contexts from the cache at a time.</span></span> <span data-ttu-id="839cc-108">No entanto, o aplicativo deve continuar a liberar esses contextos de dispositivo após o uso.</span><span class="sxs-lookup"><span data-stu-id="839cc-108">However, the application must continue to release these device contexts after use.</span></span> <span data-ttu-id="839cc-109">Como novos contextos de dispositivo de exibição para o cache são alocados no espaço de heap do aplicativo, a falha ao liberar os contextos de dispositivo eventualmente consome todo o espaço de heap disponível.</span><span class="sxs-lookup"><span data-stu-id="839cc-109">Because new display device contexts for the cache are allocated in the application's heap space, failing to release the device contexts eventually consumes all available heap space.</span></span> <span data-ttu-id="839cc-110">O sistema indica essa falha retornando um erro quando não é possível alocar espaço para o novo contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="839cc-110">The system indicates this failure by returning an error when it cannot allocate space for the new device context.</span></span> <span data-ttu-id="839cc-111">Outras funções não relacionadas ao cache também podem retornar erros.</span><span class="sxs-lookup"><span data-stu-id="839cc-111">Other functions unrelated to the cache may also return errors.</span></span>

 

 



