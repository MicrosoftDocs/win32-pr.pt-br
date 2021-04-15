---
title: Inicialização de fita
description: Um aplicativo deve usar a função CreateFile para criar um identificador de um dispositivo de fita. Esse identificador é usado em operações subsequentes na fita do dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Backup de inicialização de fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454205"
---
# <a name="tape-initialization"></a>Inicialização de fita

Um aplicativo deve usar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para criar um identificador de um dispositivo de fita. Esse identificador é usado em operações subsequentes na fita do dispositivo.

Antes que um aplicativo grave em uma fita, a fita deve ser formatada de acordo com as necessidades do aplicativo e os recursos da unidade de fita que está sendo usada. A função [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) reformata uma fita, criando um determinado número de partições de um tamanho especificado.

A função [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara uma fita para ser acessada ou removida. Essa função pode carregar, descarregar, bloquear ou desbloquear uma fita. Essa função também pode esticar a fita movendo a fita para o fim da fita e de volta para o início.

Para recuperar e definir informações sobre uma fita e uma unidade de fita, um aplicativo usa as funções [**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**setfitaparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)e [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .

[**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera informações que descrevem uma fita ou uma unidade de fita. As informações da fita incluem o tipo, a densidade e o tamanho do bloco da fita; o número de partições na fita; a quantidade de fitas restantes; e assim por diante. As informações da unidade de fita incluem o tamanho do bloco padrão da unidade, a contagem máxima de partições e os recursos com suporte.

[**Setfitaparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) define o tamanho do bloco de fita ou define os sinalizadores de unidade de fita que indicam se a unidade dá suporte a correção de erro de hardware, compactação de dados, enchimento de dados ou qualquer combinação dos três.

[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indica se a unidade de fita está pronta para processar comandos de fita.

 

 