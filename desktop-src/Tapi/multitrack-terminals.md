---
description: A TAPI 3,1 apresenta a noção de um terminal multitrack, um terminal que, em essência, é uma coleção de &\# 0034; track&\# 0034; terminais.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminais multitrack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9e5f9c6d614308370b3d9211f578d5fcb2650bd3c5ba7f8a81dbc981ad2687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575516"
---
# <a name="multitrack-terminals"></a>Terminais multitrack

A TAPI 3,1 apresenta a noção de um terminal multitrack, um terminal que, em essência, é uma coleção de terminais de "Track". Os terminais multitrack facilitam a carga do programador em situações em que vários fluxos de mídia estão envolvidos em uma sessão de comunicações.

O [terminal de gravação de arquivo](file-playback-terminal-and-file-recording-terminal.md) é um exemplo de um terminal multitrack. Ele consiste em "trilhas", onde cada "Track" é um terminal correspondente a um fluxo no arquivo gravado.

Um [terminal de faixa](track-terminals.md) pode ser outro terminal multitrack ou um terminal de controle único. Um terminal de controle único é um terminal que não possui terminais de faixa. Um terminal de controle único é um terminal no sentido TAPI 3 da palavra.

Para obter mais informações sobre terminais multitrack, consulte os seguintes tópicos:

-   [Sobre terminais multitrack](about-multitrack-terminals.md)
-   [Mecanismo de seleção de terminal padrão](default-terminal-selection-mechanism.md)
-   [Seleção de terminal manual](manual-terminal-selection.md)
-   [Usando terminais multitrack e o mecanismo de seleção padrão](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



