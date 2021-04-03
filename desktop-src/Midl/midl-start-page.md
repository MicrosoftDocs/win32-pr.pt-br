---
title: linguagem IDL da Microsoft
description: O linguagem IDL da Microsoft (MIDL) define as interfaces entre os programas cliente e servidor.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL, (consulte linguagem IDL da Microsoft MIDL)
- MIDL de linguagem IDL da Microsoft
- MIDL linguagem IDL da Microsoft, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007445"
---
# <a name="microsoft-interface-definition-language"></a><span data-ttu-id="7da3d-107">linguagem IDL da Microsoft</span><span class="sxs-lookup"><span data-stu-id="7da3d-107">Microsoft Interface Definition Language</span></span>

## <a name="purpose"></a><span data-ttu-id="7da3d-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="7da3d-108">Purpose</span></span>

<span data-ttu-id="7da3d-109">O linguagem IDL da Microsoft (MIDL) define as interfaces entre os programas cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="7da3d-109">The Microsoft Interface Definition Language (MIDL) defines interfaces between client and server programs.</span></span> <span data-ttu-id="7da3d-110">A Microsoft inclui o compilador MIDL com o SDK (Software Development Kit) da plataforma para permitir que os desenvolvedores criem os arquivos IDL (Interface Definition Language) e os ACF (arquivos de configuração de aplicativo) necessários para as interfaces RPC (chamada de procedimento remoto) e interfaces COM/DCOM.</span><span class="sxs-lookup"><span data-stu-id="7da3d-110">Microsoft includes the MIDL compiler with the Platform Software Development Kit (SDK) to enable developers to create the interface definition language (IDL) files and application configuration files (ACF) required for remote procedure call (RPC) interfaces and COM/DCOM interfaces.</span></span> <span data-ttu-id="7da3d-111">O MIDL também dá suporte à geração de bibliotecas de tipos para automação OLE.</span><span class="sxs-lookup"><span data-stu-id="7da3d-111">MIDL also supports the generation of type libraries for OLE Automation.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7da3d-112">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="7da3d-112">Where applicable</span></span>

<span data-ttu-id="7da3d-113">O MIDL pode ser usado em todos os aplicativos cliente/servidor baseados em sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="7da3d-113">MIDL can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="7da3d-114">Ele também pode ser usado para criar programas de cliente e servidor para ambientes de rede heterogêneos que incluem sistemas operacionais como UNIX e Apple.</span><span class="sxs-lookup"><span data-stu-id="7da3d-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span> <span data-ttu-id="7da3d-115">A Microsoft dá suporte ao grupo aberto (anteriormente conhecido como o padrão DCE da Open Software Foundation) para a interoperabilidade RPC.</span><span class="sxs-lookup"><span data-stu-id="7da3d-115">Microsoft supports the Open Group (formerly known as the Open Software Foundation) DCE standard for RPC interoperability.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7da3d-116">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="7da3d-116">Developer audience</span></span>

<span data-ttu-id="7da3d-117">Ao usar MIDL com RPC, familiaridade com programação C/C++ e o paradigma de RPC é necessária.</span><span class="sxs-lookup"><span data-stu-id="7da3d-117">When using MIDL with RPC, familiarity with C/C++ programming and the RPC paradigm is required.</span></span> <span data-ttu-id="7da3d-118">Ao usar MIDL com com, familiaridade com programação em C++ e o paradigma de RPC como se aplica ao COM é necessária ou, como alternativa, familiaridade com scripts de modelo de automação OLE e bibliotecas de tipos é necessária.</span><span class="sxs-lookup"><span data-stu-id="7da3d-118">When using MIDL with COM, familiarity with C++ programming and the RPC paradigm as it applies to COM is required, or alternatively, familiarity with OLE Automation model scripting and type libraries is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7da3d-119">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7da3d-119">Run-time requirements</span></span>

<span data-ttu-id="7da3d-120">As bibliotecas de tempo de execução apropriadas para usar o MIDL estão incluídas no Windows.</span><span class="sxs-lookup"><span data-stu-id="7da3d-120">The appropriate run-time libraries for using MIDL are included with Windows.</span></span> <span data-ttu-id="7da3d-121">O compilador MIDL e os componentes do ambiente de desenvolvimento RPC são instalados quando você instala o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7da3d-121">The MIDL compiler and the components of the RPC development environment are installed when you install the Windows SDK.</span></span> <span data-ttu-id="7da3d-122">Para obter mais informações, consulte [usando o compilador MIDL](using-the-midl-compiler-2.md) e [instalando o ambiente de programação RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="7da3d-122">For more information, see [Using the MIDL Compiler](using-the-midl-compiler-2.md) and [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7da3d-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7da3d-123">In this section</span></span>



| <span data-ttu-id="7da3d-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="7da3d-124">Topic</span></span>                                                                                               | <span data-ttu-id="7da3d-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="7da3d-125">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7da3d-126">Visão geral</span><span class="sxs-lookup"><span data-stu-id="7da3d-126">Overview</span></span>](about-this-guide-2.md)<br/>                                                       | <span data-ttu-id="7da3d-127">Informações gerais sobre MIDL e o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="7da3d-127">General information about MIDL and the MIDL compiler.</span></span><br/>                   |
| [<span data-ttu-id="7da3d-128">Usando o compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="7da3d-128">Using the MIDL Compiler</span></span>](using-the-midl-compiler-2.md)<br/>                                 | <span data-ttu-id="7da3d-129">Informações sobre como usar o compilter MIDL para gerar stubs RPC.</span><span class="sxs-lookup"><span data-stu-id="7da3d-129">Information about using the MIDL compilter to generate RPC stubs.</span></span><br/>       |
| [<span data-ttu-id="7da3d-130">Definições de interface e bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="7da3d-130">Interface Definitions and Type Libraries</span></span>](interface-definitions-and-type-libraries.md)<br/> | <span data-ttu-id="7da3d-131">Documentação de definições de interface específicas de RPC e bibliotecas de tipos.</span><span class="sxs-lookup"><span data-stu-id="7da3d-131">Documentation of RPC-specific interface definitions and type libraries.</span></span><br/> |
| [<span data-ttu-id="7da3d-132">Referência de Command-Line de MIDL</span><span class="sxs-lookup"><span data-stu-id="7da3d-132">MIDL Command-Line Reference</span></span>](midl-command-line-reference.md)<br/>                           | <span data-ttu-id="7da3d-133">Documentação das opções de linha de comando do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="7da3d-133">Documentation of the MIDL compiler command-line switches.</span></span><br/>               |
| [<span data-ttu-id="7da3d-134">Referência da linguagem MIDL</span><span class="sxs-lookup"><span data-stu-id="7da3d-134">MIDL Language Reference</span></span>](midl-language-reference.md)<br/>                                   | <span data-ttu-id="7da3d-135">A referência de linguagem do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="7da3d-135">The MIDL compiler language reference.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="7da3d-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7da3d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7da3d-137">RPC (chamada de procedimento remoto)</span><span class="sxs-lookup"><span data-stu-id="7da3d-137">Remote Procedure Call (RPC)</span></span>](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

