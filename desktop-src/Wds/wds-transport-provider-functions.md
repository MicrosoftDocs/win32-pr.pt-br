---
title: Funções do provedor de transporte do WDS
description: Os provedores de conteúdo definidos pelo usuário podem expor as seguintes funções de retorno de chamada para o servidor de multicast.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637020"
---
# <a name="wds-transport-provider-functions"></a><span data-ttu-id="3997b-103">Funções do provedor de transporte do WDS</span><span class="sxs-lookup"><span data-stu-id="3997b-103">WDS Transport Provider Functions</span></span>

<span data-ttu-id="3997b-104">Os provedores de conteúdo definidos pelo usuário podem expor as seguintes funções de retorno de chamada para o servidor de multicast.</span><span class="sxs-lookup"><span data-stu-id="3997b-104">User-defined content providers can expose the following callback functions to the multicast server.</span></span>



| <span data-ttu-id="3997b-105">Função</span><span class="sxs-lookup"><span data-stu-id="3997b-105">Function</span></span>                                                                               | <span data-ttu-id="3997b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3997b-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3997b-107">*WdsTransportProviderCloseContent*</span><span class="sxs-lookup"><span data-stu-id="3997b-107">*WdsTransportProviderCloseContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | <span data-ttu-id="3997b-108">Fecha um fluxo de conteúdo especificado por um identificador.</span><span class="sxs-lookup"><span data-stu-id="3997b-108">Closes a content stream specified by a handle.</span></span>                                                                          |
| [<span data-ttu-id="3997b-109">*WdsTransportProviderCloseInstance*</span><span class="sxs-lookup"><span data-stu-id="3997b-109">*WdsTransportProviderCloseInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | <span data-ttu-id="3997b-110">Fecha uma instância de um provedor de conteúdo especificado por um identificador.</span><span class="sxs-lookup"><span data-stu-id="3997b-110">Closes an instance of a content provider specified by a handle.</span></span>                                                         |
| [<span data-ttu-id="3997b-111">*WdsTransportProviderCompareContent*</span><span class="sxs-lookup"><span data-stu-id="3997b-111">*WdsTransportProviderCompareContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | <span data-ttu-id="3997b-112">Compara um nome de conteúdo e uma instância especificados para um fluxo de conteúdo aberto para determinar se eles são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="3997b-112">Compares a specified content name and instance to an open content stream to determine if they are the same.</span></span>             |
| [<span data-ttu-id="3997b-113">*WdsTransportProviderCreateInstance*</span><span class="sxs-lookup"><span data-stu-id="3997b-113">*WdsTransportProviderCreateInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | <span data-ttu-id="3997b-114">Abre uma nova instância de um provedor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3997b-114">Opens a new instance of a content provider.</span></span>                                                                             |
| [<span data-ttu-id="3997b-115">*WdsTransportProviderDumpState*</span><span class="sxs-lookup"><span data-stu-id="3997b-115">*WdsTransportProviderDumpState*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | <span data-ttu-id="3997b-116">Instrui o provedor de transporte a imprimir um resumo de seu estado e qualquer outra informação relevante para o log de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="3997b-116">Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.</span></span> |
| [<span data-ttu-id="3997b-117">*WdsTransportProviderGetContentMetadata*</span><span class="sxs-lookup"><span data-stu-id="3997b-117">*WdsTransportProviderGetContentMetadata*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | <span data-ttu-id="3997b-118">Recupera metadados para um fluxo de conteúdo aberto.</span><span class="sxs-lookup"><span data-stu-id="3997b-118">Retrieves metadata for an open content stream.</span></span>                                                                          |
| [<span data-ttu-id="3997b-119">*WdsTransportProviderGetContentSize*</span><span class="sxs-lookup"><span data-stu-id="3997b-119">*WdsTransportProviderGetContentSize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | <span data-ttu-id="3997b-120">Recupera o tamanho de um fluxo de conteúdo aberto.</span><span class="sxs-lookup"><span data-stu-id="3997b-120">Retrieves the size of an open content stream.</span></span>                                                                           |
| [<span data-ttu-id="3997b-121">*WdsTransportProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="3997b-121">*WdsTransportProviderInitialize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | <span data-ttu-id="3997b-122">Inicializa um provedor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3997b-122">Initializes a content provider.</span></span>                                                                                         |
| [<span data-ttu-id="3997b-123">*WdsTransportProviderOpenContent*</span><span class="sxs-lookup"><span data-stu-id="3997b-123">*WdsTransportProviderOpenContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | <span data-ttu-id="3997b-124">Abre uma nova exibição estática de um fluxo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3997b-124">Opens a new static view of a content stream.</span></span>                                                                            |
| [<span data-ttu-id="3997b-125">*WdsTransportProviderReadContent*</span><span class="sxs-lookup"><span data-stu-id="3997b-125">*WdsTransportProviderReadContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | <span data-ttu-id="3997b-126">Lê o conteúdo de um fluxo de conteúdo aberto.</span><span class="sxs-lookup"><span data-stu-id="3997b-126">Reads content from an open content stream.</span></span>                                                                              |
| [<span data-ttu-id="3997b-127">*WdsTransportProviderRefreshSettings*</span><span class="sxs-lookup"><span data-stu-id="3997b-127">*WdsTransportProviderRefreshSettings*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | <span data-ttu-id="3997b-128">Instrui o provedor de transporte a ler novamente as configurações relevantes.</span><span class="sxs-lookup"><span data-stu-id="3997b-128">Instructs the transport provider to reread any relevant settings.</span></span>                                                       |
| [<span data-ttu-id="3997b-129">*WdsTransportProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="3997b-129">*WdsTransportProviderShutdown*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | <span data-ttu-id="3997b-130">Shutsdown o provedor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3997b-130">Shutsdown the content provider.</span></span>                                                                                         |
| [<span data-ttu-id="3997b-131">*WdsTransportProviderUserAccessCheck*</span><span class="sxs-lookup"><span data-stu-id="3997b-131">*WdsTransportProviderUserAccessCheck*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | <span data-ttu-id="3997b-132">Especifica o acesso a um fluxo de conteúdo com base no token de um usuário.</span><span class="sxs-lookup"><span data-stu-id="3997b-132">Specifies access to a content stream based on a user's token.</span></span>                                                           |



 

 

 




