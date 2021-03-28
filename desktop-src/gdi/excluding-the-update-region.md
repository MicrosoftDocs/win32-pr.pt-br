---
description: A função ExcludeUpdateRgn exclui a região de atualização da região de recorte para o contexto do dispositivo de vídeo.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Excluindo a região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010730"
---
# <a name="excluding-the-update-region"></a><span data-ttu-id="3178f-103">Excluindo a região de atualização</span><span class="sxs-lookup"><span data-stu-id="3178f-103">Excluding the Update Region</span></span>

<span data-ttu-id="3178f-104">A função [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) exclui a região de atualização da região de recorte para o contexto do dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3178f-104">The [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) function excludes the update region from the clipping region for the display device context.</span></span> <span data-ttu-id="3178f-105">Essa função é útil ao desenhar em uma janela diferente de quando uma mensagem do WM \_ Paint está sendo processada.</span><span class="sxs-lookup"><span data-stu-id="3178f-105">This function is useful when drawing in a window other than when a WM\_PAINT message is processing.</span></span> <span data-ttu-id="3178f-106">Ele impede o desenho nas áreas que serão atualizadas durante a próxima mensagem do WM \_ Paint.</span><span class="sxs-lookup"><span data-stu-id="3178f-106">It prevents drawing in the areas that will be updated during the next WM\_PAINT message.</span></span>

 

 



