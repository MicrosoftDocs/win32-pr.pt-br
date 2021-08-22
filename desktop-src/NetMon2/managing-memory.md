---
description: Caso um especialista falhe durante o tempo de execução, se você usar Monitor de Rede funções para gerenciamento de memória, Monitor de Rede liberará a memória alocada.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gerenciando memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4cc5b38f5525b7c0d19e115c83ed9f770c72215c6b64825a089ec389bfc09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555876"
---
# <a name="managing-memory"></a>Gerenciando memória

Caso um especialista falhe durante o tempo de execução, se você usar Monitor de Rede funções para gerenciamento de memória, Monitor de Rede liberará a memória alocada. No entanto, quando você escreve um especialista, pode ser necessário adquirir recursos do sistema e informações da estrutura de dados. Por exemplo, o especialista de União de protocolo Monitor de Rede adquire um identificador de arquivo para criar uma nova captura. Cada especialista deve criar seu próprio tratamento **try/catch** para que o especialista possa liberar recursos adquiridos.

Quando a memória for alocada, use as seguintes funções de memória existentes:

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



