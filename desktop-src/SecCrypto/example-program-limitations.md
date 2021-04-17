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
# <a name="example-program-limitations"></a><span data-ttu-id="ddab8-103">Limitações do programa de exemplo</span><span class="sxs-lookup"><span data-stu-id="ddab8-103">Example Program Limitations</span></span>

<span data-ttu-id="ddab8-104">Os princípios de boa prática de programação nem sempre são seguidos nesses programas de exemplo para fornecer um código mais conciso e mais legível.</span><span class="sxs-lookup"><span data-stu-id="ddab8-104">Principles of good programming practice are not always followed in these sample programs in order to provide more concise, more readable code.</span></span> <span data-ttu-id="ddab8-105">Especialmente:</span><span class="sxs-lookup"><span data-stu-id="ddab8-105">In particular:</span></span>

-   <span data-ttu-id="ddab8-106">Somente respostas de erro limitadas são mostradas.</span><span class="sxs-lookup"><span data-stu-id="ddab8-106">Only limited error responses are shown.</span></span> <span data-ttu-id="ddab8-107">Os programas de trabalho sempre devem verificar os códigos de erro retornados e executar as ações apropriadas quando um erro for encontrado.</span><span class="sxs-lookup"><span data-stu-id="ddab8-107">Working programs should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="ddab8-108">Somente a memória limitada e o gerenciamento de recursos são feitos.</span><span class="sxs-lookup"><span data-stu-id="ddab8-108">Only limited memory and resource management is done.</span></span> <span data-ttu-id="ddab8-109">Em programas em funcionamento, todas as chaves e [*hashes*](../secgloss/h-gly.md) devem ser destruídos, toda a memória alocada deve ser liberada, todos os arquivos devem ser fechados e todos os identificadores devem ser liberados.</span><span class="sxs-lookup"><span data-stu-id="ddab8-109">In working programs, all keys and [*hashes*](../secgloss/h-gly.md) should be destroyed, all allocated memory should be freed, all files should be closed, and all handles should be released.</span></span> <span data-ttu-id="ddab8-110">Esses programas de exemplo fornecem apenas demonstrações limitadas do uso de funções que executam essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="ddab8-110">These example programs provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="ddab8-111">Esses programas de exemplo não executam tarefas de gerenciamento de recursos ou memória no caso de encerramento do programa devido a erros.</span><span class="sxs-lookup"><span data-stu-id="ddab8-111">These example programs perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

 

 
