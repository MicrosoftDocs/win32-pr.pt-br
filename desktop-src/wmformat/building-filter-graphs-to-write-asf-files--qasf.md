---
title: Criando gráficos de filtro para gravar arquivos ASF (QASF)
description: Criando gráficos de filtro para gravar arquivos ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows SDK do formato de mídia, criando gráficos de filtro (QASF)
- Windows SDK do formato de mídia, DirectShow
- Windows Media Format SDK, gravando arquivos ASF (QASF)
- ASF (Advanced Systems Format), criando gráficos de filtro (QASF)
- ASF (formato de sistemas avançados), criando gráficos de filtro (QASF)
- ASF (Advanced Systems Format), gravação (QASF)
- ASF (formato de sistemas avançados), gravação (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, criando gráficos de filtro (QASF)
- DirectShow, gravando arquivos ASF (QASF)
- Windows SDK do formato de mídia, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6128fb7578d829579aad7e8895be9db4d5a842aa785866253b553d4deb8b3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055576"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>Criando gráficos de filtro para gravar arquivos ASF (QASF)

aplicativos baseados em DirectShow normalmente usam um dos três tipos básicos de grafos de filtro ao criar Windows conteúdo baseado em mídia:

-   filtrar grafos para converter ou transcodificar conteúdo de algum outro formato no formato de mídia Windows.
-   filtrar grafos para inserir conteúdo que não seja Windows com base em mídia (formatos de fluxo nativos) em arquivos ASF.
-   filtrar grafos para capturar dados dinâmicos e codificá-los imediatamente no formato de mídia Windows antes de salvá-los no disco.

Cada tipo de grafo de filtro é descrito mais detalhadamente nas seções a seguir.



| Seção                                                                                                             | Descrição                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Transcodificação de arquivos (QASF)](transcoding-files--qasf.md)                                                             | Descreve como criar gráficos de filtro de transcodificação de arquivo.                                               |
| [Inserindo formatos de fluxo nativos em arquivos ASF (QASF)](inserting-native-stream-formats-into-asf-files--qasf.md)   | Descreve como posicionar qualquer tipo de áudio compactado ou não compactado ou dados de vídeo em um arquivo ASF. |
| [Capturando diretamente de um dispositivo para um arquivo ASF (QASF)](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | Descreve como criar gráficos de filtro de captura que geram saída para um arquivo ASF.                             |



 

 

 




