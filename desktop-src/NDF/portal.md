---
title: Estrutura de diagnóstico de rede
description: O NDF (estrutura de diagnóstico de rede) fornece uma maneira para que os desenvolvedores de componentes e aplicativos simplifiquem a solução de problemas de rede para os usuários.
ms.assetid: 61dfb66b-4bc6-43a9-ad61-698f5cd67f4a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0342ee4cb285f0a0f1c76c74b3bdc5b412b07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005225"
---
# <a name="network-diagnostics-framework"></a><span data-ttu-id="6a7d9-103">Estrutura de diagnóstico de rede</span><span class="sxs-lookup"><span data-stu-id="6a7d9-103">Network Diagnostics Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="6a7d9-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="6a7d9-104">Purpose</span></span>

<span data-ttu-id="6a7d9-105">O NDF (estrutura de diagnóstico de rede) fornece uma maneira para que os desenvolvedores de componentes e aplicativos simplifiquem a solução de problemas de rede para os usuários.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-105">The Network Diagnostics Framework (NDF) provides a way for component and application developers to simplify network troubleshooting for users.</span></span> <span data-ttu-id="6a7d9-106">Os usuários podem tentar diagnosticar e reparar um problema de rede usando uma única ferramenta de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-106">Users can attempt to diagnose and repair a network problem using a single troubleshooting tool.</span></span>

<span data-ttu-id="6a7d9-107">A Microsoft fornece classes auxiliares NDF, algumas das quais são extensíveis para que os desenvolvedores possam criar unidades de solução de problemas chamadas de extensões de classe auxiliar para fornecer diagnósticos mais detalhados específicos para determinados componentes de software ou hardware.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-107">Microsoft provides NDF helper classes, some of which are extensible so that developers can create troubleshooting units called helper class extensions to provide more detailed diagnoses specific to particular software or hardware components.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6a7d9-108">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="6a7d9-108">Where applicable</span></span>

<span data-ttu-id="6a7d9-109">O NDF pode ser usado por qualquer software de fornecedor que dependa da conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-109">NDF can be used by any vendor's software which relies on network connectivity.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6a7d9-110">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="6a7d9-110">Developer audience</span></span>

<span data-ttu-id="6a7d9-111">A API NDF foi projetada para desenvolvedores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-111">The NDF API is designed for C/C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6a7d9-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="6a7d9-112">Run-time requirements</span></span>

<span data-ttu-id="6a7d9-113">O NDF está disponível para computadores que executam o Windows Vista, o Windows Server 2008 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-113">NDF is available for computers running Windows Vista, Windows Server 2008, or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6a7d9-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6a7d9-114">In this section</span></span>



| <span data-ttu-id="6a7d9-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="6a7d9-115">Topic</span></span>                                                                       | <span data-ttu-id="6a7d9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a7d9-116">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a7d9-117">Sobre NDF</span><span class="sxs-lookup"><span data-stu-id="6a7d9-117">About NDF</span></span>](about-ndf.md)<br/>                                       | <span data-ttu-id="6a7d9-118">Fornece um resumo geral da tecnologia NDF.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-118">Provides a general summary of the NDF technology.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="6a7d9-119">Usando NDF</span><span class="sxs-lookup"><span data-stu-id="6a7d9-119">Using NDF</span></span>](using-ndf.md)<br/>                                       | <span data-ttu-id="6a7d9-120">Fornece informações e exemplos sobre como usar a funcionalidade NDF, bem como estender essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-120">Provides information and examples on using NDF functionality, as well as how to extend this functionality.</span></span><br/>                                                                                    |
| [<span data-ttu-id="6a7d9-121">Referência de NDF</span><span class="sxs-lookup"><span data-stu-id="6a7d9-121">NDF Reference</span></span>](ndf-reference.md)<br/>                               | <span data-ttu-id="6a7d9-122">Fornece informações sobre enumerações, funções, interfaces e estruturas que dão suporte ao uso de NDF, bem como informações sobre as classes auxiliares extensíveis fornecidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-122">Provides information about enumerations, functions, interfaces, and structures that support the use of NDF, as well as information about the extensible helper classes provided by Microsoft.</span></span><br/> |
| [<span data-ttu-id="6a7d9-123">Rastreamento de rede no Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a7d9-123">Network Tracing in Windows 7</span></span>](network-tracing-in-windows-7.md)<br/> | <span data-ttu-id="6a7d9-124">Discute o rastreamento de rede e as ferramentas a serem usadas para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="6a7d9-124">Discusses network tracing and tools to use for troubleshooting.</span></span><br/>                                                                                                                               |



 

 

 





