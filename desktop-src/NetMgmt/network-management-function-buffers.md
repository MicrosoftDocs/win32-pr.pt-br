---
title: Buffers de função de gerenciamento de rede
description: A biblioteca de tempo de execução RPC manipula os buffers exigidos pelas funções de gerenciamento de rede de recuperação de dados de 32 bits da seguinte maneira.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159955"
---
# <a name="network-management-function-buffers"></a><span data-ttu-id="0470f-103">Buffers de função de gerenciamento de rede</span><span class="sxs-lookup"><span data-stu-id="0470f-103">Network Management Function Buffers</span></span>

<span data-ttu-id="0470f-104">A biblioteca de tempo de execução RPC manipula os buffers exigidos pelas funções de gerenciamento de rede de recuperação de dados de 32 bits da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0470f-104">The RPC run-time library handles the buffers required by the 32-bit data retrieval network management functions as follows:</span></span>

-   <span data-ttu-id="0470f-105">**Enviando dados para o servidor** (dados especificados por \[ em \] parâmetros).</span><span class="sxs-lookup"><span data-stu-id="0470f-105">**Sending data to the server** (data specified by \[in\] parameters).</span></span>

    <span data-ttu-id="0470f-106">O chamador deve alocar e desalocar o buffer para a estrutura de informações relevante (ou estruturas) e passar uma variável de ponteiro para a função.</span><span class="sxs-lookup"><span data-stu-id="0470f-106">The caller must allocate and deallocate the buffer for the relevant information structure (or structures) and pass a pointer variable to the function.</span></span> <span data-ttu-id="0470f-107">O chamador não precisa especificar o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="0470f-107">The caller does not need to specify the buffer length.</span></span>

    <span data-ttu-id="0470f-108">Exemplo: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span><span class="sxs-lookup"><span data-stu-id="0470f-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span></span>

-   <span data-ttu-id="0470f-109">**Recuperando dados do servidor** (dados especificados por \[ parâmetros de saída \] ).</span><span class="sxs-lookup"><span data-stu-id="0470f-109">**Retrieving data from the server** (data specified by \[out\] parameters).</span></span>

    <span data-ttu-id="0470f-110">O sistema aloca o buffer para as informações retornadas.</span><span class="sxs-lookup"><span data-stu-id="0470f-110">The system allocates the buffer for the returned information.</span></span> <span data-ttu-id="0470f-111">O chamador deve passar uma variável de ponteiro para a função na entrada.</span><span class="sxs-lookup"><span data-stu-id="0470f-111">The caller must pass a pointer variable to the function on input.</span></span> <span data-ttu-id="0470f-112">Após o retorno bem-sucedido, o ponteiro recebe o endereço do buffer alocado pelo sistema que contém as informações retornadas.</span><span class="sxs-lookup"><span data-stu-id="0470f-112">On successful return, the pointer receives the address of the system-allocated buffer that contains the returned information.</span></span> <span data-ttu-id="0470f-113">Isso simplifica o código de chamada, porque o chamador não precisa estimar o tamanho do buffer ou redimensionar o buffer e emitir a função novamente.</span><span class="sxs-lookup"><span data-stu-id="0470f-113">This simplifies the calling code, because the caller does not need to estimate the size of the buffer, or resize the buffer and reissue the function.</span></span>

    <span data-ttu-id="0470f-114">Quando o chamador terminar de processar as informações retornadas, ele deverá liberar a memória alocada pelo sistema chamando a função [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) .</span><span class="sxs-lookup"><span data-stu-id="0470f-114">When the caller has finished processing the returned information, it must free the system-allocated memory by calling the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function.</span></span> <span data-ttu-id="0470f-115">Para obter mais informações sobre como especificar tamanhos de buffer, consulte [comprimentos de buffer de função de gerenciamento de rede](network-management-function-buffer-lengths.md).</span><span class="sxs-lookup"><span data-stu-id="0470f-115">For more information about specifying buffer sizes, see [Network Management Function Buffer Lengths](network-management-function-buffer-lengths.md).</span></span>

    <span data-ttu-id="0470f-116">Exemplo: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span><span class="sxs-lookup"><span data-stu-id="0470f-116">Example: [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span></span>

 

 




