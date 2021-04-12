---
title: Sobre o Gerenciador de compactação de vídeo
description: Sobre o Gerenciador de compactação de vídeo
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Multimídia do Windows, Gerenciador de compactação de vídeo (VCM)
- multimídia, Gerenciador de compactação de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454022"
---
# <a name="about-the-video-compression-manager"></a>Sobre o Gerenciador de compactação de vídeo

Normalmente, os compactadores instaláveis operam com dados de imagem de vídeo armazenados em arquivos AVI (áudio-vídeo intercalado). Esta visão geral explica as técnicas de programação usadas para acessar os compactadores instaláveis por meio do VCM e aborda os seguintes tópicos:

-   VCM e a arquitetura de vídeo para Windows
-   Compactando e descompactando dados de imagem do seu aplicativo
-   Usando renderizadores VCM para desenhar dados de seu aplicativo
-   Funções e estruturas do VCM

Antes de ler esta visão geral, você deve estar familiarizado com os serviços gráficos do Microsoft Win32. Em particular, bitmaps e estruturas relacionadas a bitmaps, como [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) e [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), são usados extensivamente pelo VCM. Para obter informações adicionais sobre as estruturas **BITMAPINFO** e **BITMAPINFOHEADER** , consulte [bitmaps](/previous-versions//ms532349(v=vs.85)).

> [!Note]  
> O Gerenciador de compactação de áudio (ACM) fornece suporte de nível de sistema para drivers de compactação e descompactação de áudio. Para obter uma descrição dos serviços de compactação de áudio, consulte [Gerenciador de compactação de áudio](audio-compression-manager.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> </dl>

 

 