---
description: Sobre dispositivos de captura de vídeo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Sobre dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645868"
---
# <a name="about-video-capture-devices"></a>Sobre dispositivos de captura de vídeo

A maioria dos novos dispositivos de captura de vídeo usam drivers de Windows Driver Model (WDM). Na arquitetura WDM, a Microsoft fornece um conjunto de drivers independentes de hardware, chamados de drivers de classe, e o fornecedor de hardware fornece minidrivers específicas de hardware. Um minidriver implementa qualquer função que seja específica para o dispositivo; para a maioria das funções, o minidriver chama o Microsoft Class Driver.

Em um grafo de filtro do DirectShow, qualquer dispositivo de captura WDM aparece como o filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) . O filtro de captura de vídeo WDM se configura com base nas características do driver. Ele aparece sob um nome fornecido pelo driver — você não verá um filtro chamado "filtro de captura de vídeo WDM" em qualquer lugar no grafo.

Alguns dispositivos de captura mais antigos ainda usam drivers de vídeo para Windows (VFW). Embora esses drivers agora sejam obsoletos, eles têm suporte no DirectShow por meio do filtro de [captura VFW](vfw-capture-filter.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a captura de vídeo no DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



