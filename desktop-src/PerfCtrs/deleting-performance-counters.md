---
description: Para remover os contadores de desempenho de aplicativos do sistema, execute as etapas a seguir.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Excluindo contadores de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756704"
---
# <a name="deleting-performance-counters"></a><span data-ttu-id="85d09-103">Excluindo contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="85d09-103">Deleting Performance Counters</span></span>

<span data-ttu-id="85d09-104">Para remover os contadores de desempenho do aplicativo do sistema, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="85d09-104">To remove your application's performance counters from the system, perform the following steps.</span></span>

1.  <span data-ttu-id="85d09-105">Use a ferramenta **Unlodctr** incluída no computador para remover os dados relacionados ao contador do registro.</span><span class="sxs-lookup"><span data-stu-id="85d09-105">Use the **unlodctr** tool included with the computer to remove the counter related data from the registry.</span></span> <span data-ttu-id="85d09-106">Observe que a chave de **desempenho** do aplicativo deve existir para que a ferramenta **Unlodctr** seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="85d09-106">Note that the application's **Performance** key must exist for the **unlodctr** tool to succeed.</span></span> <span data-ttu-id="85d09-107">Para obter detalhes, consulte [removendo nomes de contadores e descrições do registro](removing-counter-names-and-descriptions-from-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="85d09-107">For details, see [Removing Counter Names and Descriptions from the Registry](removing-counter-names-and-descriptions-from-the-registry.md).</span></span>
2.  <span data-ttu-id="85d09-108">Exclua as chaves de **desempenho** e **vinculação** na chave de **Serviços** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85d09-108">Delete the **Performance** and **Linkage** keys under the application's **Services** key.</span></span> <span data-ttu-id="85d09-109">Para excluir essas chaves, use o utilitário Regedt32.exe ou chame [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span><span class="sxs-lookup"><span data-stu-id="85d09-109">To delete these keys, use either the Regedt32.exe utility or call [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span></span>

 

 
