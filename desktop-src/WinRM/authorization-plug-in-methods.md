---
title: Métodos de plug-in de autorização
description: Todos os pontos de entrada de plug-in de autorização têm um mecanismo de retorno de chamada para relatar o êxito ou a falha da chamada. Alguns mecanismos de retorno de chamada são chamados várias vezes até que todos os resultados sejam relatados.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790639"
---
# <a name="authorization-plug-in-methods"></a><span data-ttu-id="91830-104">Métodos de plug-in de autorização</span><span class="sxs-lookup"><span data-stu-id="91830-104">Authorization Plug-in Methods</span></span>

<span data-ttu-id="91830-105">Todos os pontos de entrada de plug-in de autorização têm um mecanismo de retorno de chamada para relatar o êxito ou a falha da chamada.</span><span class="sxs-lookup"><span data-stu-id="91830-105">All authorization plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="91830-106">Alguns mecanismos de retorno de chamada são chamados várias vezes até que todos os resultados sejam relatados.</span><span class="sxs-lookup"><span data-stu-id="91830-106">Some callback mechanisms are called multiple times until all of the results are reported.</span></span>

<span data-ttu-id="91830-107">A tabela a seguir fornece uma visão geral dos métodos de retorno de chamada de autorização.</span><span class="sxs-lookup"><span data-stu-id="91830-107">The following table provides an overview of the authorization callback methods.</span></span>



| <span data-ttu-id="91830-108">Método</span><span class="sxs-lookup"><span data-stu-id="91830-108">Method</span></span>                                                                           | <span data-ttu-id="91830-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="91830-109">Description</span></span>                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="91830-110">**WSManPluginAuthzOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="91830-110">**WSManPluginAuthzOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | <span data-ttu-id="91830-111">Relata uma operação de usuário bem-sucedida ou com falha.</span><span class="sxs-lookup"><span data-stu-id="91830-111">Reports either a successful or failed user operation.</span></span>                |
| [<span data-ttu-id="91830-112">**WSManPluginAuthzQueryQuotaComplete**</span><span class="sxs-lookup"><span data-stu-id="91830-112">**WSManPluginAuthzQueryQuotaComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | <span data-ttu-id="91830-113">Relata os detalhes de cota que são relevantes para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="91830-113">Reports quota details that are relevant for the specified user.</span></span>      |
| [<span data-ttu-id="91830-114">**WSManPluginAuthzUserComplete**</span><span class="sxs-lookup"><span data-stu-id="91830-114">**WSManPluginAuthzUserComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | <span data-ttu-id="91830-115">Relata uma autorização de conexão de usuário com êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="91830-115">Reports either a successful or failed user connection authorization.</span></span> |



 

 

 




