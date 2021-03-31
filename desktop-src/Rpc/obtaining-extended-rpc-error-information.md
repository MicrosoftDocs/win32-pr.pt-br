---
title: Obtendo informações estendidas de erro RPC
description: O RPC fornece a capacidade de obter informações de erro estendidas. Esta seção descreve como essas informações de erro podem ser obtidas e oferece recomendações sobre como usar as informações.
ms.assetid: 7a386def-c640-42f4-9869-b6a1c522984a
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, informações de erro estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7856dd76a86763fc3f537577f9c547508fbf34ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635874"
---
# <a name="obtaining-extended-rpc-error-information"></a><span data-ttu-id="cb374-105">Obtendo informações estendidas de erro RPC</span><span class="sxs-lookup"><span data-stu-id="cb374-105">Obtaining Extended RPC Error Information</span></span>

<span data-ttu-id="cb374-106">O RPC fornece a capacidade de obter informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="cb374-106">RPC provides the capability to obtain extended error information.</span></span> <span data-ttu-id="cb374-107">Esta seção descreve como essas informações de erro podem ser obtidas e oferece recomendações sobre como usar as informações.</span><span class="sxs-lookup"><span data-stu-id="cb374-107">This section describes how such error information can be obtained, and offers recommendations on how to use the information.</span></span>

<span data-ttu-id="cb374-108">Esta seção é dividida nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="cb374-108">This section is broken into the following topics:</span></span>

-   [<span data-ttu-id="cb374-109">A necessidade de informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="cb374-109">The Need For Extended Error Information</span></span>](the-need-for-extended-error-information.md)
-   [<span data-ttu-id="cb374-110">Informações de segurança e de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="cb374-110">Security and Extended Error Information</span></span>](security-and-extended-error-information.md)
-   [<span data-ttu-id="cb374-111">Habilitando informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="cb374-111">Enabling Extended Error Information</span></span>](enabling-extended-error-information.md)
-   [<span data-ttu-id="cb374-112">Noções básicas sobre informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="cb374-112">Understanding Extended Error Information</span></span>](understanding-extended-error-information.md)
-   [<span data-ttu-id="cb374-113">Confiabilidade das informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="cb374-113">Reliability of Extended Error Information</span></span>](reliability-of-extended-error-information.md)
-   [<span data-ttu-id="cb374-114">Independência de outros componentes</span><span class="sxs-lookup"><span data-stu-id="cb374-114">Independence From Other Components</span></span>](independence-from-other-components.md)
-   [<span data-ttu-id="cb374-115">Informações de erro estendidas para o usuário</span><span class="sxs-lookup"><span data-stu-id="cb374-115">Extended Error Information for the User</span></span>](extended-error-information-for-the-user.md)
-   [<span data-ttu-id="cb374-116">Informações de erro estendidas para o servidor ou aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb374-116">Extended Error Information for the Server or Application</span></span>](extended-error-information-for-the-server-or-application.md)
-   [<span data-ttu-id="cb374-117">Locais de detecção de informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="cb374-117">Extended Error Information Detection Locations</span></span>](extended-error-information-detection-locations.md)

<span data-ttu-id="cb374-118">Esta seção está fortemente ligada à depuração do aplicativo RPC.</span><span class="sxs-lookup"><span data-stu-id="cb374-118">This section is closely tied with RPC application debugging.</span></span> <span data-ttu-id="cb374-119">Para obter informações adicionais sobre a depuração RPC, consulte \[ pacote do depurador \] .</span><span class="sxs-lookup"><span data-stu-id="cb374-119">For additional information about RPC debugging, see \[debugger package\].</span></span>

 

 




