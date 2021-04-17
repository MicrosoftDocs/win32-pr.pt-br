---
description: Per-Pixel mesclagem alfa
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel mesclagem alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789826"
---
# <a name="per-pixel-alpha-blending"></a>Per-Pixel mesclagem alfa

Quatro subtipos de mídia foram definidos para mesclagem alfa por pixel. Esses subtipos só têm suporte quando o VMR está no modo de mistura. O VMR rejeitará a conexão se não estiver no modo de mistura quando um filtro upstream tentar se conectar usando um desses subtipos. Esses subtipos são definidos em UUIDs. h:

-   MEDIASUBTYPE \_ ARGB1555
-   MEDIASUBTYPE \_ ARGB4444
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ AYUV

Para obter mais informações, consulte [subtipos de vídeo RGB não compactados](uncompressed-rgb-video-subtypes.md) e [**subtipos de vídeo YUV**](yuv-video-subtypes.md).

 

 



