---
description: Limitações do programa de exemplo
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitações do programa de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769286"
---
# <a name="example-program-limitations"></a>Limitações do programa de exemplo

Os princípios de boa prática de programação nem sempre são seguidos nesses programas de exemplo para fornecer um código mais conciso e mais legível. Especialmente:

-   Somente respostas de erro limitadas são mostradas. Os programas de trabalho sempre devem verificar os códigos de erro retornados e executar as ações apropriadas quando um erro for encontrado.
-   Somente a memória limitada e o gerenciamento de recursos são feitos. Em programas em funcionamento, todas as chaves e [*hashes*](../secgloss/h-gly.md) devem ser destruídos, toda a memória alocada deve ser liberada, todos os arquivos devem ser fechados e todos os identificadores devem ser liberados. Esses programas de exemplo fornecem apenas demonstrações limitadas do uso de funções que executam essas tarefas. Esses programas de exemplo não executam tarefas de gerenciamento de recursos ou memória no caso de encerramento do programa devido a erros.

 

 
