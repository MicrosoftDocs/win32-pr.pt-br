---
title: FAZER interfaces
description: Use as seguintes interfaces de otimização de entrega (DO) para transferir arquivos e monitorar trabalhos na fila de transferência.
ms.assetid: 20203CCD-86CC-4551-BA4F-0A5999F8C956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0359328f189c1a5b5d9649d8300dc59a80df4480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813458"
---
# <a name="do-interfaces"></a>FAZER interfaces

Use as seguintes interfaces de otimização de entrega (DO) para transferir arquivos e monitorar trabalhos na fila de transferência.

| Interface | Descrição |
|-|-|
| [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) | Os clientes implementam a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para receber a notificação de que um trabalho foi concluído, foi modificado ou está com erro. |
| [**IBackgroundCopyError**](ibackgroundcopyerror.md) | Recupera detalhes de um erro de trabalho. |
| [**IBackgroundCopyFile**](ibackgroundcopyfile.md) | Recupera os nomes de arquivo local e remoto de uma solicitação de transferência de arquivo no trabalho e seu progresso. |
| [**IBackgroundCopyFile2**](ibackgroundcopyfile2.md) | Especifica um novo nome remoto para o arquivo e recupera a lista de intervalos a serem baixados. |
| [**IBackgroundCopyFile5**](ibackgroundcopyfile5.md) | Fornece métodos get e set de propriedade genérica para propriedades BackgroundCopyFile. |
| [**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md) | Adiciona arquivos ao trabalho, define o nível de prioridade do trabalho, determina o estado do trabalho e inicia e para o trabalho. |
| [**IBackgroundCopyJob5**](ibackgroundcopyjob5.md) | Consulta ou define vários comportamentos opcionais de um trabalho. |
| [**IBackgroundCopyManager**](ibackgroundcopymanager.md) | Cria trabalhos de transferência, recupera um objeto de enumerador de trabalhos na fila e recupera trabalhos individuais da fila. |
| [**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md) | Use para baixar intervalos de um arquivo. |
| [**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md) | Use para identificar o status de um arquivo específico. |
| [**IDODownload**](./do/nn-do-idodownload.md) | Usado para iniciar e gerenciar um download. |
| [**IDODownloadInternal**](./dodownloadinternal/nn-dodownloadinternal-idodownloadinternal.md) | Usado para obter ou definir propriedades de download estendido. |
| [**IDODownloadStatusCallback**](./do/nn-do-idodownloadstatuscallback.md) | Usado para receber notificações sobre um download. |
| [**IDOManager**](./do/nn-do-idomanager.md) | Usado para criar um novo download e para enumerar downloads existentes. |
| [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) | Enumera os arquivos no trabalho. |