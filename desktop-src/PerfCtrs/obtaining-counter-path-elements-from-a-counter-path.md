---
description: Para recuperar os elementos de um caminho, chame a função PdhParseCounterPath. A função analisa os elementos de um caminho de contador e os retorna em uma estrutura de elementos de caminho do contador de PDH \_ \_ \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtendo elementos do caminho do contador a partir de um caminho do contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778702"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a><span data-ttu-id="3a3bf-104">Obtendo elementos do caminho do contador a partir de um caminho do contador</span><span class="sxs-lookup"><span data-stu-id="3a3bf-104">Obtaining Counter Path Elements from a Counter Path</span></span>

<span data-ttu-id="3a3bf-105">Para recuperar os elementos de um caminho, chame a função [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) .</span><span class="sxs-lookup"><span data-stu-id="3a3bf-105">To retrieve the elements of a path, call the [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) function.</span></span> <span data-ttu-id="3a3bf-106">A função analisa os elementos de um caminho de contador e os retorna em uma estrutura de [**elementos de caminho do contador de PDH \_ \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .</span><span class="sxs-lookup"><span data-stu-id="3a3bf-106">The function parses the elements of a counter path and returns them in a [**PDH\_COUNTER\_PATH\_ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) structure.</span></span>

<span data-ttu-id="3a3bf-107">Se você tiver um nome de instância complexo (um que contenha uma instância pai e um índice de instância), você poderá chamar a função [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) para extrair o nome da instância, o índice da instância e o nome do pai.</span><span class="sxs-lookup"><span data-stu-id="3a3bf-107">If you have a complex instance name (one that contains a parent instance and instance index), you can call the [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) function to extract the instance name, instance index, and parent name.</span></span>

 

 



