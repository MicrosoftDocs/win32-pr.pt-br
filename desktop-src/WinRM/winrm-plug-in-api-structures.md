---
title: Estruturas de API de plug-in do WinRM
description: Estruturas de API de plug-in do WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292509"
---
# <a name="winrm-plug-in-api-structures"></a><span data-ttu-id="aa47b-103">Estruturas de API de plug-in do WinRM</span><span class="sxs-lookup"><span data-stu-id="aa47b-103">WinRM Plug-in API Structures</span></span>

<span data-ttu-id="aa47b-104">A tabela a seguir fornece uma visão geral das estruturas na API (interface de programação de aplicativo) do plug-in do Gerenciamento Remoto do Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="aa47b-104">The following table provides an overview of the structures in the Windows Remote Management (WinRM) plug-in application programming interface (API).</span></span>



| <span data-ttu-id="aa47b-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="aa47b-105">Structure</span></span>                                                        | <span data-ttu-id="aa47b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa47b-106">Description</span></span>                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa47b-107">**cota do WSMAN \_ AUTHZ \_**</span><span class="sxs-lookup"><span data-stu-id="aa47b-107">**WSMAN\_AUTHZ\_QUOTA**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | <span data-ttu-id="aa47b-108">Define informações de cotas para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="aa47b-108">Defines quota information on a per-user basis.</span></span>                                           |
| [<span data-ttu-id="aa47b-109">**\_detalhes do certificado WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="aa47b-109">**WSMAN\_CERTIFICATE\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | <span data-ttu-id="aa47b-110">Representa os campos dentro do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="aa47b-110">Represents the fields within the client certificate.</span></span>                                     |
| [<span data-ttu-id="aa47b-111">**\_conjunto de \_ ARG de comando WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="aa47b-111">**WSMAN\_COMMAND\_ARG\_SET**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | <span data-ttu-id="aa47b-112">Representa o conjunto de argumentos que são passados para a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="aa47b-112">Represents the set of arguments that are passed in to the command line.</span></span>                  |
| [<span data-ttu-id="aa47b-113">**\_filtro WSMan**</span><span class="sxs-lookup"><span data-stu-id="aa47b-113">**WSMAN\_FILTER**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | <span data-ttu-id="aa47b-114">Define a filtragem usada para uma operação.</span><span class="sxs-lookup"><span data-stu-id="aa47b-114">Defines the filtering used for an operation.</span></span>                                             |
| [<span data-ttu-id="aa47b-115">**fragmento do WSMAN \_**</span><span class="sxs-lookup"><span data-stu-id="aa47b-115">**WSMAN\_FRAGMENT**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | <span data-ttu-id="aa47b-116">Define as informações de fragmento para uma operação.</span><span class="sxs-lookup"><span data-stu-id="aa47b-116">Defines the fragment information for an operation.</span></span>                                       |
| [<span data-ttu-id="aa47b-117">**\_informações da operação do WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="aa47b-117">**WSMAN\_OPERATION\_INFO**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | <span data-ttu-id="aa47b-118">Representa um ponto de extremidade de recurso específico para o qual o plug-in deve executar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="aa47b-118">Represents a specific resource end-point for which the plug-in must perform the request.</span></span> |
| [<span data-ttu-id="aa47b-119">**\_solicitação de plug-in do WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="aa47b-119">**WSMAN\_PLUGIN\_REQUEST**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | <span data-ttu-id="aa47b-120">Contém informações sobre a solicitação e é passado para cada operação de plug-in.</span><span class="sxs-lookup"><span data-stu-id="aa47b-120">Contains information about the request and is passed into every plug-in operation.</span></span>       |
| [<span data-ttu-id="aa47b-121">**\_detalhes do remetente WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="aa47b-121">**WSMAN\_SENDER\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | <span data-ttu-id="aa47b-122">Especifica os detalhes do cliente para cada solicitação de entrada.</span><span class="sxs-lookup"><span data-stu-id="aa47b-122">Specifies client details for every inbound request.</span></span>                                      |



 

 

 




