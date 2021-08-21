---
description: Sobre dispositivos de captura de vídeo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Sobre dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff3fff9f3d009006e300afdbe9986bfdc8d0a32ea618fdd2748efe0bd650b5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160179"
---
# <a name="about-video-capture-devices"></a>Sobre dispositivos de captura de vídeo

a maioria dos novos dispositivos de captura de vídeo usam drivers de Windows Driver Model (WDM). Na arquitetura WDM, a Microsoft fornece um conjunto de drivers independentes de hardware, chamados de drivers de classe, e o fornecedor de hardware fornece minidrivers específicas de hardware. Um minidriver implementa qualquer função que seja específica para o dispositivo; para a maioria das funções, o minidriver chama o Microsoft Class Driver.

em um DirectShow gráfico de filtro, qualquer dispositivo de captura wdm aparece como o filtro de [captura de vídeo wdm](wdm-video-capture-filter.md) . O filtro de captura de vídeo WDM se configura com base nas características do driver. Ele aparece sob um nome fornecido pelo driver — você não verá um filtro chamado "filtro de captura de vídeo WDM" em qualquer lugar no grafo.

alguns dispositivos de captura mais antigos ainda usam vídeo para drivers de Windows (VFW). embora esses drivers agora sejam obsoletos, eles têm suporte no DirectShow por meio do filtro de [captura VFW](vfw-capture-filter.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a captura de vídeo no DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



