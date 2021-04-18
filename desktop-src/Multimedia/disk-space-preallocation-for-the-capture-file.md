---
title: Alocação de espaço em disco para o arquivo de captura
description: Alocação de espaço em disco para o arquivo de captura
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE mensagem
- macro capFileAlloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292096"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Alocação de espaço em disco para o arquivo de captura

A alocação de espaço em disco para o arquivo de captura cria um arquivo de um tamanho especificado no disco antes do início de uma operação de captura. A alocação de um arquivo de captura reduz o processamento necessário enquanto a captura está em andamento e resulta em menos quadros descartados. Você pode prealocar um arquivo de captura usando a mensagem de [**alocação de arquivo do WM \_ \_ \_ Cap**](wm-cap-file-allocate.md) (ou a macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ).

Normalmente, seu aplicativo deve prealocar espaço em disco suficiente para conter o maior arquivo de captura previsto. A alocação de espaço em disco não restringe o tamanho do arquivo capturado. O tamanho do arquivo será automaticamente ampliado se os dados capturados excederem o espaço alocado. As operações de gravação subsequentes no arquivo de captura reutilizam as partes do espaço em disco alocadas para o arquivo, preservando o tamanho e a fragmentação do arquivo.

Você também pode melhorar o desempenho de captura desfragmentando o arquivo de captura. Para desfragmentar o arquivo, use um utilitário de desfragmentação, como o Desfragmentador de disco. Se você usar um arquivo de captura desfragmentado e mais tarde aumentá-lo, Desfragmente o arquivo ampliado. A ampliação de um arquivo de captura desfragmentado pode fragmentar a parte expandida do arquivo e reduzir o desempenho na operação de captura.

Você também pode melhorar o desempenho usando um disco descompactado para captura de vídeo. A compactação de dados durante a captura pode limitar a taxa de transferência de captura para o disco.

Um aplicativo pode reservar um arquivo de captura permanente para eliminar o tempo necessário para prealocar e desfragmentar um arquivo toda vez que ele for iniciado. Como um arquivo de captura pode exigir um espaço considerável em disco e a alocação de um arquivo de captura remove todos os dados de um arquivo de captura existente, um aplicativo deve permitir que o usuário decida se o arquivo é permanente ou temporário.

 

 




