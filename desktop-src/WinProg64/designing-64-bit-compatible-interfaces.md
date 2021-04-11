---
title: Criando interfaces compatíveis com 64 bits
description: Problemas de compatibilidade com versões anteriores surgem quando você adiciona novos tipos de dados ou métodos a uma interface, altera tipos de dados antigos ou usa tipos de dados inadequadamente.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- compatibilidade com versões anteriores programação de 64 bits do Windows
- interfaces compatíveis com 64 bits – programação de 64 bits do Windows
- Guia de programação do Windows de 64 bits, programação do Windows de 64 bits, compatibilidade
- compatibilidade 64-programação do Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292142"
---
# <a name="designing-64-bit-compatible-interfaces"></a><span data-ttu-id="503d8-107">Criando interfaces compatíveis com 64 bits</span><span class="sxs-lookup"><span data-stu-id="503d8-107">Designing 64-bit-Compatible Interfaces</span></span>

<span data-ttu-id="503d8-108">A portabilidade de janelas de 32 bits para o Windows de 64 bits não deve, por si só, criar problemas para aplicativos distribuídos, se eles usam RPC (chamadas de procedimento remoto) diretamente ou por DCOM.</span><span class="sxs-lookup"><span data-stu-id="503d8-108">Porting from 32-bit Windows to 64-bit Windows should not, by itself, create any problems for distributed applications, whether they use Remote Procedure Calls (RPC) directly or through DCOM.</span></span> <span data-ttu-id="503d8-109">O modelo de programação RPC especifica os tamanhos de dados e tipos inteiros bem definidos que têm o mesmo tamanho em cada extremidade da conexão.</span><span class="sxs-lookup"><span data-stu-id="503d8-109">The RPC programming model specifies well-defined data sizes and integer types that are the same size on each end of the connection.</span></span> <span data-ttu-id="503d8-110">Além disso, no modelo de dados abstrato LLP64 desenvolvido para o Windows de 64 bits, somente os ponteiros se expandem para 64 bits – todos os outros tipos de dados inteiros permanecem 32 bits.</span><span class="sxs-lookup"><span data-stu-id="503d8-110">Also, in the LLP64 abstract data model developed for 64-bit Windows, only the pointers expand to 64 bits—all other integer data types remain 32 bits.</span></span> <span data-ttu-id="503d8-111">Como os ponteiros são locais para cada lado da conexão de cliente/servidor e geralmente são transmitidos como marcadores **nulos** ou não **nulos** , o mecanismo de marshaling pode manipular diferentes tamanhos de ponteiro em qualquer extremidade de uma conexão de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="503d8-111">Because pointers are local to each side of the client/server connection and are usually transmitted as **NULL** or non-**NULL** markers, the marshaling engine can handle different pointer sizes on either end of a connection transparently.</span></span>

<span data-ttu-id="503d8-112">No entanto, problemas de compatibilidade com versões anteriores surgem quando você adiciona novos tipos de dados ou métodos a uma interface, altera tipos de dados antigos ou usa tipos de dados inadequadamente.</span><span class="sxs-lookup"><span data-stu-id="503d8-112">However, backward compatibility issues arise when you add new data types or methods to an interface, change old data types, or use data types inappropriately.</span></span> <span data-ttu-id="503d8-113">Os tópicos a seguir discutem como evitar essas situações (quando possível) e como criar soluções alternativas robustas quando não é possível evitá-las.</span><span class="sxs-lookup"><span data-stu-id="503d8-113">The following topics discuss how to avoid these situations (when possible) and how to design robust workarounds when it is not possible to avoid them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="503d8-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="503d8-114">In this Section</span></span>

-   [<span data-ttu-id="503d8-115">Alterando uma interface existente</span><span class="sxs-lookup"><span data-stu-id="503d8-115">Changing an Existing Interface</span></span>](changing-an-existing-interface.md)
-   [<span data-ttu-id="503d8-116">Evitando a ocultação de informações</span><span class="sxs-lookup"><span data-stu-id="503d8-116">Avoiding Information Hiding</span></span>](avoiding-information-hiding.md)
-   [<span data-ttu-id="503d8-117">Evitando o polimorfismo</span><span class="sxs-lookup"><span data-stu-id="503d8-117">Avoiding Polymorphism</span></span>](avoiding-polymorphism.md)
-   [<span data-ttu-id="503d8-118">Usando novos tipos de dados em seu arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="503d8-118">Using New Data Types in Your IDL File</span></span>](using-new-data-types-in-your-idl-file.md)
-   [<span data-ttu-id="503d8-119">Preparando seu aplicativo para o Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="503d8-119">Preparing Your Application for 64-bit Windows</span></span>](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a><span data-ttu-id="503d8-120">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="503d8-120">Related Sections</span></span>

<span data-ttu-id="503d8-121">Se você ainda não estiver familiarizado com os novos tipos de dados, o ambiente de trabalho e as alterações de API para o Windows de 64 bits, consulte [preparando-se para o Windows de 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="503d8-121">If you are not already familiar with the new data types, working environment, and API changes for 64-bit Windows, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

 

 




