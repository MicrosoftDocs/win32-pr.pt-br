---
description: Monitor de Rede captura o tráfego de rede para exibição e análise. Ele permite que você execute tarefas como analisar dados capturados anteriormente em métodos definidos pelo usuário e extrair dados de analisadores de protocolo definidos.
ms.assetid: a70b6e22-e744-4760-b878-9ee35428fed5
title: Monitor de Rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51a57dd2373d7a10fedd68a72dbc4021efdb921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506091"
---
# <a name="network-monitor"></a><span data-ttu-id="01971-104">Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="01971-104">Network Monitor</span></span>

## <a name="purpose"></a><span data-ttu-id="01971-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="01971-105">Purpose</span></span>

<span data-ttu-id="01971-106">Monitor de Rede captura o tráfego de rede para exibição e análise.</span><span class="sxs-lookup"><span data-stu-id="01971-106">Network Monitor captures network traffic for display and analysis.</span></span> <span data-ttu-id="01971-107">Ele permite que você execute tarefas como analisar dados capturados anteriormente em métodos definidos pelo usuário e extrair dados de analisadores de protocolo definidos.</span><span class="sxs-lookup"><span data-stu-id="01971-107">It enables you to perform tasks such as analyzing previously captured data in user-defined methods and extract data from defined protocol parsers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="01971-108">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="01971-108">Developer audience</span></span>

<span data-ttu-id="01971-109">Todos os conjuntos de API fornecidos pelo Monitor de Rede podem ser acessados usando C/C++.</span><span class="sxs-lookup"><span data-stu-id="01971-109">All API sets provided by Network Monitor can be accessed using C/C++.</span></span> <span data-ttu-id="01971-110">Esses desenvolvedores também trabalhando com [*provedores de pacotes de rede*](n.md) também devem estar familiarizados COM o com.</span><span class="sxs-lookup"><span data-stu-id="01971-110">Those developers also working with [*network packet providers*](n.md) must also be familiar with COM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="01971-111">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="01971-111">Run-time requirements</span></span>

<span data-ttu-id="01971-112">Para chamar da API de Monitor de Rede, você deve estar executando o Windows NT Server 4,0, o Windows 2000 Server ou o Windows Server 2003 ou ter o Microsoft Systems Management Server instalado.</span><span class="sxs-lookup"><span data-stu-id="01971-112">To call from the Network Monitor API, you must be running on Windows NT Server 4.0, Windows 2000 Server, or Windows Server 2003, or have Microsoft Systems Management Server installed.</span></span>

<span data-ttu-id="01971-113">O driver NPP e os recursos com suporte incluem todas as versões do Windows NT 4,0 e do Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="01971-113">The NPP driver and supported features include all versions of Windows NT 4.0 and Windows 2000 Server.</span></span>

> [!Note]  
> <span data-ttu-id="01971-114">Monitor de Rede 2,1 e versões anteriores não têm suporte no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="01971-114">Network Monitor 2.1 and earlier are not supported on Windows Vista and later.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="01971-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="01971-115">In this section</span></span>



| <span data-ttu-id="01971-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="01971-116">Topic</span></span>                                                                 | <span data-ttu-id="01971-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="01971-117">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01971-118">O SDK do Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="01971-118">The Network Monitor SDK</span></span>](the-network-monitor-sdk.md)<br/>     | <span data-ttu-id="01971-119">Introdução ao SDK do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="01971-119">Introduction to the Network Monitor SDK.</span></span><br/>                                                   |
| [<span data-ttu-id="01971-120">Sobre o Monitor de Rede 2,1</span><span class="sxs-lookup"><span data-stu-id="01971-120">About Network Monitor 2.1</span></span>](about-network-monitor-2-1.md)<br/> | <span data-ttu-id="01971-121">Conceitos e serviços do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="01971-121">Network Monitor concepts and services.</span></span><br/>                                                     |
| [<span data-ttu-id="01971-122">Usando o Monitor de Rede 2,1</span><span class="sxs-lookup"><span data-stu-id="01971-122">Using Network Monitor 2.1</span></span>](using-network-monitor-2-1.md)<br/> | <span data-ttu-id="01971-123">Tópicos relacionados a tarefas que descrevem como usar funções de Monitor de Rede e componentes COM.</span><span class="sxs-lookup"><span data-stu-id="01971-123">Task-related topics that describe how to use Network Monitor functions and COM components.</span></span><br/> |
| [<span data-ttu-id="01971-124">Referência</span><span class="sxs-lookup"><span data-stu-id="01971-124">Reference</span></span>](reference.md)<br/>                                 | <span data-ttu-id="01971-125">Tópicos de referência para Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="01971-125">Reference topics for Network Monitor.</span></span><br/>                                                      |
| [<span data-ttu-id="01971-126">Glossário</span><span class="sxs-lookup"><span data-stu-id="01971-126">Glossary</span></span>](glossary.md)<br/>                                   | <span data-ttu-id="01971-127">Definições e terminologia para Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="01971-127">Definitions and terminology for Network Monitor.</span></span><br/>                                           |



 

 

 




