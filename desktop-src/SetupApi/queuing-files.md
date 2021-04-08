---
description: Depois de obter um identificador para uma fila de arquivos chamando a função SetupOpenFileQueue, você pode adicionar operações de arquivo à fila, arquivo por arquivo ou enfileirando todos os arquivos em uma seção INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Enfileirando arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828540"
---
# <a name="queuing-files"></a>Enfileirando arquivos

Depois de obter um identificador para uma fila de arquivos chamando a função [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) , você pode adicionar operações de arquivo à fila, arquivo por arquivo ou enfileirando todos os arquivos em uma seção inf.

Para adicionar uma operação de cópia para um arquivo individual à fila de arquivos, chame a função [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) . Se você quiser enfileirar uma operação de cópia de arquivo usando a mídia de origem padrão e os destinos de destino especificados em um arquivo INF, você pode chamar a função [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .

Você pode adicionar uma operação individual de exclusão ou renomeação de arquivo à fila de arquivos aberta, chamando a função [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) ou [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .

 

 



