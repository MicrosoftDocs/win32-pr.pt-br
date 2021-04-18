---
title: Criando gráficos de filtro para gravar arquivos ASF (QASF)
description: Criando gráficos de filtro para gravar arquivos ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- SDK do Windows Media Format, criando gráficos de filtro (QASF)
- SDK do Windows Media Format, DirectShow
- Windows Media Format SDK, gravando arquivos ASF (QASF)
- ASF (Advanced Systems Format), criando gráficos de filtro (QASF)
- ASF (formato de sistemas avançados), criando gráficos de filtro (QASF)
- ASF (Advanced Systems Format), gravação (QASF)
- ASF (formato de sistemas avançados), gravação (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, criação de gráficos de filtro (QASF)
- DirectShow, gravando arquivos ASF (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764236"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>Criando gráficos de filtro para gravar arquivos ASF (QASF)

Aplicativos baseados no DirectShow normalmente usam um dos três tipos básicos de grafos de filtro ao criar conteúdo baseado no Windows Media:

-   Filtrar grafos para converter ou transcodificar conteúdo de outro formato no formato de mídia do Windows.
-   Filtrar grafos para inserir conteúdo que não seja baseado no Windows Media (formatos de fluxo nativos) em arquivos ASF.
-   Filtrar grafos para capturar dados dinâmicos e codificá-los imediatamente no formato de mídia do Windows antes de salvá-los no disco.

Cada tipo de grafo de filtro é descrito mais detalhadamente nas seções a seguir.



| Seção                                                                                                             | Descrição                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Transcodificação de arquivos (QASF)](transcoding-files--qasf.md)                                                             | Descreve como criar gráficos de filtro de transcodificação de arquivo.                                               |
| [Inserindo formatos de fluxo nativos em arquivos ASF (QASF)](inserting-native-stream-formats-into-asf-files--qasf.md)   | Descreve como posicionar qualquer tipo de áudio compactado ou não compactado ou dados de vídeo em um arquivo ASF. |
| [Capturando diretamente de um dispositivo para um arquivo ASF (QASF)](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | Descreve como criar gráficos de filtro de captura que geram saída para um arquivo ASF.                             |



 

 

 




