---
title: Pré-alocação de espaço em disco para o arquivo de captura
description: Pré-alocação de espaço em disco para o arquivo de captura
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE mensagem
- macro capFileAlloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687a14fa0f3a01a65ad2cb90062fcd4e237eb3e94ef99460d77883bd26df9213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678756"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Pré-alocação de espaço em disco para o arquivo de captura

A pré-localização do espaço em disco para o arquivo de captura cria um arquivo de um tamanho especificado no disco antes do início de uma operação de captura. A pré-localização de um arquivo de captura reduz o processamento necessário enquanto a captura está em andamento e resulta em menos quadros descartados. Você pode pré-alocar um arquivo de captura usando a mensagem [**WM \_ CAP FILE \_ \_ ALLOCATE**](wm-cap-file-allocate.md) (ou a [**macro capFileAlloc).**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc)

Normalmente, seu aplicativo deve pré-alcar espaço em disco suficiente para conter o maior arquivo de captura previsto. A pré-localização do espaço em disco não restringe o tamanho do arquivo capturado. O tamanho do arquivo será ampliado automaticamente se os dados capturados excederem o espaço alocado. As operações de gravação subsequentes no arquivo de captura reutilizarão as partes de espaço em disco alocadas para o arquivo, preservando o tamanho e a fragmentação do arquivo.

Você também pode melhorar o desempenho da captura desfragmentando o arquivo de captura. Para desfragmentar o arquivo, use um utilitário de desfragmentação, como o Desfragmentador de Disco. Se você usar um arquivo de captura desfragmentado e, posteriormente, ampliá-lo, deverá desfragmentar o arquivo ampliado. Ampliar um arquivo de captura desfragmentado pode fragmentar a parte expandida do arquivo e reduzir o desempenho na operação de captura.

Você também pode melhorar o desempenho usando um disco descompactado para captura de vídeo. Compactar dados durante a captura pode limitar a produtividade da captura ao disco.

Um aplicativo pode reservar um arquivo de captura permanente para eliminar o tempo necessário para pré-locar e desfragmentar um arquivo sempre que ele é iniciado. Como um arquivo de captura pode exigir espaço em disco considerável e a pré-localização de um arquivo de captura remove todos os dados de um arquivo de captura existente, um aplicativo deve permitir que o usuário decida se o arquivo é permanente ou temporário.

 

 




