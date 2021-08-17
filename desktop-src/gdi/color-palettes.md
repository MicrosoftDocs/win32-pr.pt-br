---
description: Uma paleta de cores é uma matriz que contém valores de cor que identificam as cores que podem ser exibidas ou desenhadas no dispositivo de saída no momento.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: paletas de cores (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81079ac94b40de98bc1c53098a8b9d1654f90d0d855397ac38d11311e9741e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761953"
---
# <a name="color-palettes-windows-gdi"></a>paletas de cores (Windows GDI)

Uma paleta de cores é uma matriz que contém valores de cor que identificam as cores que podem ser exibidas ou desenhadas no dispositivo de saída no momento. As paletas de cores são usadas por dispositivos que são capazes de gerar muitas cores, mas que só podem exibir ou desenhar um subconjunto deles em um determinado momento. Para esses dispositivos, o sistema mantém uma *paleta do sistema* para acompanhar e gerenciar as cores atuais do dispositivo. Os aplicativos não têm acesso direto à paleta do sistema. Em vez disso, o sistema associa uma paleta padrão a cada contexto de dispositivo. Os aplicativos podem usar as cores na paleta padrão ou definir suas próprias cores criando *paletas lógicas* e associando-as a contextos de dispositivo individuais.

Um aplicativo pode determinar se um dispositivo dá suporte a paletas de cores verificando o \_ bit da paleta RC no valor RasterCaps retornado pela função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .

 

 



