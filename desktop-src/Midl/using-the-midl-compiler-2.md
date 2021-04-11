---
title: Usando o compilador MIDL
description: O compilador MIDL é instalado automaticamente como parte da instalação do SDK (Software Development Kit) da plataforma.
ms.assetid: 6c001b06-01f3-42bd-85db-5d53aab54903
keywords:
- Linguagem IDL da Microsoft MIDL, tarefas
- MIDL do compilador MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fd6630a8e3fcb5c46325b5258da567fcbd0eec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365963"
---
# <a name="using-the-midl-compiler"></a><span data-ttu-id="f49d9-105">Usando o compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="f49d9-105">Using the MIDL Compiler</span></span>

<span data-ttu-id="f49d9-106">O compilador MIDL é instalado automaticamente como parte da instalação do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="f49d9-106">The MIDL compiler is automatically installed as part of the Platform Software Development Kit (SDK) setup.</span></span> <span data-ttu-id="f49d9-107">Os tópicos a seguir descrevem os requisitos do compilador C MIDL e do pré-processador do C, as bibliotecas de links que fazem parte do produto RPC (chamada de procedimento remoto) e os arquivos gerados pelo MIDL para interfaces DCOM, interfaces RPC e interfaces de biblioteca de tipos de automação OLE.</span><span class="sxs-lookup"><span data-stu-id="f49d9-107">The following topics describe the MIDL C compiler and C preprocessor requirements, the link libraries that are part of the Remote Procedure Call (RPC) product, and the files that MIDL generates for DCOM interfaces, RPC interfaces, and OLE Automation type library interfaces.</span></span>

-   [<span data-ttu-id="f49d9-108">Invocando o compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="f49d9-108">Invoking the MIDL Compiler</span></span>](invoking-the-midl-compiler.md)
-   [<span data-ttu-id="f49d9-109">Arquivos de resposta</span><span class="sxs-lookup"><span data-stu-id="f49d9-109">Response Files</span></span>](response-files.md)
-   [<span data-ttu-id="f49d9-110">Requisitos de pré-processador do C para MIDL</span><span class="sxs-lookup"><span data-stu-id="f49d9-110">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="f49d9-111">C/C++-considerações do compilador</span><span class="sxs-lookup"><span data-stu-id="f49d9-111">C/C++-Compiler Considerations</span></span>](c-c-compiler-considerations.md)
-   [<span data-ttu-id="f49d9-112">Usando a \_ \_ constante predefinida MIDL</span><span class="sxs-lookup"><span data-stu-id="f49d9-112">Using the \_\_midl Predefined Constant</span></span>](using-the---midl-predefined-constant.md)
-   [<span data-ttu-id="f49d9-113">MIDL e RPC</span><span class="sxs-lookup"><span data-stu-id="f49d9-113">MIDL and RPC</span></span>](midl-and-rpc.md)
-   [<span data-ttu-id="f49d9-114">MIDL e COM</span><span class="sxs-lookup"><span data-stu-id="f49d9-114">MIDL and COM</span></span>](midl-and-com.md)
-   [<span data-ttu-id="f49d9-115">MIDL e ODL</span><span class="sxs-lookup"><span data-stu-id="f49d9-115">MIDL and ODL</span></span>](midl-and-odl.md)

<span data-ttu-id="f49d9-116">Para obter mais informações sobre os arquivos que compõem o produto RPC, consulte [instalando o ambiente de programação RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="f49d9-116">For more information about the files that make up the RPC product, see [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

 

 