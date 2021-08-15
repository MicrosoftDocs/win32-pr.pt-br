---
title: Inicialização de fita
description: Um aplicativo deve usar a função CreateFile para criar um handle de um dispositivo de fita. Esse handle é usado em operações subsequentes na fita no dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Backup de inicialização de fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aeba729feb9351b5af15d26f6366b455c5ce74a9cc6300c9ab8d25047b4760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835399"
---
# <a name="tape-initialization"></a>Inicialização de fita

Um aplicativo deve usar a [**função CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para criar um handle de um dispositivo de fita. Esse handle é usado em operações subsequentes na fita no dispositivo.

Antes que um aplicativo grave em uma fita, a fita deve ser formatada de acordo com as necessidades do aplicativo e os recursos da unidade de fita que está sendo usada. A [**função CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) reformata uma fita, criando nele um determinado número de partições de um tamanho especificado.

A [**função PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara uma fita para ser acessada ou removida. Essa função pode carregar, descarregar, bloquear ou desbloquear uma fita. Essa função também pode tensão da fita movendo a fita para o final da fita e de volta para o início.

Para recuperar e definir informações sobre uma unidade de fita e fita, um aplicativo usa as funções [**GetTapeParameters,**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)e [**GetTapeStatus.**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera informações que descrevem uma fita ou uma unidade de fita. As informações de fita incluem o tipo, a densidade e o tamanho do bloco da fita; o número de partições na fita; a quantidade de fita restante; e assim por diante. As informações da unidade de fita incluem o tamanho do bloco padrão da unidade, a contagem máxima de partições e os recursos com suporte.

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) define o tamanho do bloco de fita ou define os sinalizadores de unidade de fita que indicam se a unidade dá suporte à correção de erro de hardware, compactação de dados, preenchimento de dados ou qualquer combinação dos três.

[**GetTapeStatus indica**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) se a unidade de fita está pronta para processar comandos de fita.

 

 