---
title: Métodos de plug-in de operações
description: Métodos de plug-in de operações
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915848"
---
# <a name="operations-plug-in-methods"></a><span data-ttu-id="37680-103">Métodos de plug-in de operações</span><span class="sxs-lookup"><span data-stu-id="37680-103">Operations Plug-in Methods</span></span>

<span data-ttu-id="37680-104">Todos os pontos de entrada de plug-in de operações têm um mecanismo de retorno de chamada para relatar o êxito ou a falha da chamada.</span><span class="sxs-lookup"><span data-stu-id="37680-104">All operations plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="37680-105">Alguns mecanismos de retorno de chamada são chamados várias vezes, até que todos os resultados sejam relatados.</span><span class="sxs-lookup"><span data-stu-id="37680-105">Some callback mechanisms are called multiple times, until all of the results are reported.</span></span>

<span data-ttu-id="37680-106">A tabela a seguir fornece uma visão geral dos métodos de retorno de chamada de operações.</span><span class="sxs-lookup"><span data-stu-id="37680-106">The following table provides an overview of the operations callback methods.</span></span>



| <span data-ttu-id="37680-107">Método</span><span class="sxs-lookup"><span data-stu-id="37680-107">Method</span></span>                                                                         | <span data-ttu-id="37680-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="37680-108">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37680-109">**WSManPluginFreeRequestDetails**</span><span class="sxs-lookup"><span data-stu-id="37680-109">**WSManPluginFreeRequestDetails**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | <span data-ttu-id="37680-110">Libera a memória alocada para a estrutura de [**\_ \_ solicitação de plug-in do WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .</span><span class="sxs-lookup"><span data-stu-id="37680-110">Releases memory that is allocated for the [**WSMAN\_PLUGIN\_REQUEST**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) structure.</span></span>                                          |
| [<span data-ttu-id="37680-111">**WSManPluginGetOperationParameters**</span><span class="sxs-lookup"><span data-stu-id="37680-111">**WSManPluginGetOperationParameters**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | <span data-ttu-id="37680-112">Obtém informações operacionais, tais como tempos limite e restrições de dados associadas a uma operação.</span><span class="sxs-lookup"><span data-stu-id="37680-112">Gets operational information, such as time-outs and data restrictions that are associated with an operation.</span></span>                                         |
| [<span data-ttu-id="37680-113">**WSManPluginOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="37680-113">**WSManPluginOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | <span data-ttu-id="37680-114">Registra a conclusão de uma operação.</span><span class="sxs-lookup"><span data-stu-id="37680-114">Records the completion of an operation.</span></span>                                                                                                              |
| [<span data-ttu-id="37680-115">**WSManPluginReceiveResult**</span><span class="sxs-lookup"><span data-stu-id="37680-115">**WSManPluginReceiveResult**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | <span data-ttu-id="37680-116">Relata resultados para Gerenciamento Remoto do Windows (WinRM) plug-ins.</span><span class="sxs-lookup"><span data-stu-id="37680-116">Reports results to Windows Remote Management (WinRM) plug-ins.</span></span>                                                                                       |
| [<span data-ttu-id="37680-117">**WSManPluginReportContext**</span><span class="sxs-lookup"><span data-stu-id="37680-117">**WSManPluginReportContext**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | <span data-ttu-id="37680-118">Relata o Shell e o contexto de comando de volta para a infraestrutura do WinRM para que outras operações possam ser executadas em relação ao shell e/ou ao comando.</span><span class="sxs-lookup"><span data-stu-id="37680-118">Reports the shell and command context back to the WinRM infrastructure so that further operations can be performed against the shell and/or command.</span></span> |



 

 

 




