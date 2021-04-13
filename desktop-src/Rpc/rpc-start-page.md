---
title: Chamada de Procedimento Remoto
description: A RPC (chamada de procedimento remoto) da Microsoft define uma tecnologia poderosa para a criação de programas de cliente/servidor distribuídos.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC, (consulte chamada de procedimento remoto)
- RPC de chamada de procedimento remoto, página inicial
- RPC de chamada de procedimento remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366529"
---
# <a name="remote-procedure-call"></a><span data-ttu-id="39b40-107">Chamada de Procedimento Remoto</span><span class="sxs-lookup"><span data-stu-id="39b40-107">Remote Procedure Call</span></span>

## <a name="purpose"></a><span data-ttu-id="39b40-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="39b40-108">Purpose</span></span>

<span data-ttu-id="39b40-109">A RPC (chamada de procedimento remoto) da Microsoft define uma tecnologia poderosa para a criação de programas de cliente/servidor distribuídos.</span><span class="sxs-lookup"><span data-stu-id="39b40-109">Microsoft Remote Procedure Call (RPC) defines a powerful technology for creating distributed client/server programs.</span></span> <span data-ttu-id="39b40-110">As bibliotecas e os stubs de tempo de execução do RPC gerenciam a maioria dos processos relacionados aos protocolos de rede e à comunicação.</span><span class="sxs-lookup"><span data-stu-id="39b40-110">The RPC run-time stubs and libraries manage most of the processes relating to network protocols and communication.</span></span> <span data-ttu-id="39b40-111">Isso permite que você se concentre nos detalhes do aplicativo em vez dos detalhes da rede.</span><span class="sxs-lookup"><span data-stu-id="39b40-111">This enables you to focus on the details of the application rather than the details of the network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="39b40-112">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="39b40-112">Where applicable</span></span>

<span data-ttu-id="39b40-113">O RPC pode ser usado em todos os aplicativos cliente/servidor com base em sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="39b40-113">RPC can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="39b40-114">Ele também pode ser usado para criar programas de cliente e servidor para ambientes de rede heterogêneos que incluem sistemas operacionais como UNIX e Apple.</span><span class="sxs-lookup"><span data-stu-id="39b40-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="39b40-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="39b40-115">Developer audience</span></span>

<span data-ttu-id="39b40-116">O RPC foi projetado para ser usado por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="39b40-116">RPC is designed to be used by C/C++ programmers.</span></span> <span data-ttu-id="39b40-117">É necessário ter familiaridade com o linguagem IDL da Microsoft (MIDL) e o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="39b40-117">Familiarity with the Microsoft Interface Definition Language (MIDL) and the MIDL compiler are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="39b40-118">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="39b40-118">Run-time requirements</span></span>

<span data-ttu-id="39b40-119">As bibliotecas de tempo de execução RPC estão incluídas no Windows.</span><span class="sxs-lookup"><span data-stu-id="39b40-119">The RPC run-time libraries are included with Windows.</span></span> <span data-ttu-id="39b40-120">Os componentes do ambiente de desenvolvimento RPC são instalados quando você instala o SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="39b40-120">The components of the RPC development environment are installed when you install the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="39b40-121">Para obter detalhes, consulte [instalando o ambiente de programação RPC](installing-the-rpc-programming-environment.md).</span><span class="sxs-lookup"><span data-stu-id="39b40-121">For details, see [Installing the RPC Programming Environment](installing-the-rpc-programming-environment.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="39b40-122">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="39b40-122">In this section</span></span>



| <span data-ttu-id="39b40-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="39b40-123">Topic</span></span>                                                                           | <span data-ttu-id="39b40-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="39b40-124">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39b40-125">Melhores práticas de programação RPC</span><span class="sxs-lookup"><span data-stu-id="39b40-125">Best RPC Programming Practices</span></span>](best-rpc-programming-practices.md)<br/> | <span data-ttu-id="39b40-126">Orientação sobre as práticas de programação de RPC que ajudam a criar os melhores aplicativos RPC possíveis.</span><span class="sxs-lookup"><span data-stu-id="39b40-126">Guidance on RPC programming practices that help create the best possible RPC applications.</span></span><br/>                            |
| [<span data-ttu-id="39b40-127">Visão geral</span><span class="sxs-lookup"><span data-stu-id="39b40-127">Overview</span></span>](overviews.md)<br/>                                            | <span data-ttu-id="39b40-128">Informações gerais sobre a incorporação de RPC em seus aplicativos cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="39b40-128">General information about incorporating RPC into your client/server applications.</span></span><br/>                                     |
| [<span data-ttu-id="39b40-129">Referência</span><span class="sxs-lookup"><span data-stu-id="39b40-129">Reference</span></span>](reference.md)<br/>                                           | <span data-ttu-id="39b40-130">Documentação de tipos, funções e constantes de RPC.</span><span class="sxs-lookup"><span data-stu-id="39b40-130">Documentation of RPC types, functions, and constants.</span></span><br/>                                                                 |
| [<span data-ttu-id="39b40-131">Mecanismo de NDR de RPC</span><span class="sxs-lookup"><span data-stu-id="39b40-131">RPC NDR Engine</span></span>](rpc-ndr-engine.md)<br/>                                 | <span data-ttu-id="39b40-132">Documentação do mecanismo de marshaling para componentes RPC e DCOM, o mecanismo de representação de dados de rede (NDR) RPC.</span><span class="sxs-lookup"><span data-stu-id="39b40-132">Documentation of the marshaling engine for RPC and DCOM components, the RPC Network Data Representation (NDR) Engine.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="39b40-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39b40-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39b40-134">Linguagem IDL da Microsoft (MIDL)</span><span class="sxs-lookup"><span data-stu-id="39b40-134">Microsoft Interface Definition Language (MIDL)</span></span>](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

