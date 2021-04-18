---
description: Os aplicativos podem usar com segurança os recursos de gerenciamento de memória da biblioteca de tempo de execução do C (malloc, Free e assim por diante) e do C++ (novo, excluir e assim por diante).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funções da biblioteca C padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778742"
---
# <a name="standard-c-library-functions"></a><span data-ttu-id="ba0b8-103">Funções da biblioteca C padrão</span><span class="sxs-lookup"><span data-stu-id="ba0b8-103">Standard C Library Functions</span></span>

<span data-ttu-id="ba0b8-104">Os aplicativos podem usar com segurança os recursos de gerenciamento de memória da biblioteca de tempo de execução do C (**malloc**, **Free** e assim por diante) e do C++ (**novo**, **excluir** e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="ba0b8-104">Applications can safely use the memory management features of the C run-time library (**malloc**, **free**, and so on) and C++ (**new**, **delete**, and so on).</span></span> <span data-ttu-id="ba0b8-105">As funções de biblioteca de tempo de execução do C não têm os possíveis problemas que têm no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ba0b8-105">The C run-time library functions do not have the potential problems they have under 16-bit Windows.</span></span> <span data-ttu-id="ba0b8-106">O gerenciamento de memória não é mais um problema porque o sistema está livre para gerenciar a memória movendo as páginas da memória física sem afetar os endereços virtuais.</span><span class="sxs-lookup"><span data-stu-id="ba0b8-106">Memory management is no longer a problem because the system is free to manage memory by moving pages of physical memory without affecting the virtual addresses.</span></span> <span data-ttu-id="ba0b8-107">Da mesma forma, a distinção entre ponteiros próximos e distantes não é mais relevante.</span><span class="sxs-lookup"><span data-stu-id="ba0b8-107">Similarly, the distinction between near and far pointers is no longer relevant.</span></span> <span data-ttu-id="ba0b8-108">Portanto, você pode usar as funções da biblioteca C padrão para gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="ba0b8-108">Therefore, you can use the standard C library functions for memory management.</span></span> <span data-ttu-id="ba0b8-109">No entanto, as funções de gerenciamento de memória fornecem funcionalidade que não está disponível na biblioteca de tempo de execução do C.</span><span class="sxs-lookup"><span data-stu-id="ba0b8-109">However, the memory management functions do provide functionality that is unavailable in the C run-time library.</span></span>

 

 



