---
description: Caso um especialista falhe durante o tempo de execução, se você usar Monitor de Rede funções para gerenciamento de memória, Monitor de Rede liberará a memória alocada.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gerenciando memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921002"
---
# <a name="managing-memory"></a>Gerenciando memória

Caso um especialista falhe durante o tempo de execução, se você usar Monitor de Rede funções para gerenciamento de memória, Monitor de Rede liberará a memória alocada. No entanto, quando você escreve um especialista, pode ser necessário adquirir recursos do sistema e informações da estrutura de dados. Por exemplo, o especialista de União de protocolo Monitor de Rede adquire um identificador de arquivo para criar uma nova captura. Cada especialista deve criar seu próprio tratamento **try/catch** para que o especialista possa liberar recursos adquiridos.

Quando a memória for alocada, use as seguintes funções de memória existentes:

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



