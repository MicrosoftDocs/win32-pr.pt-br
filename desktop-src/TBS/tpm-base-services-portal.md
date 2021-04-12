---
title: Serviços base do TPM
description: O software TPM fornece serviços como uma API exposta por meio de chamada de procedimento remoto. Use o TPM para criar um módulo TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TBS dos serviços de base do TPM
- TBS de serviços base do TPM, home page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366379"
---
# <a name="tpm-base-services"></a><span data-ttu-id="fddea-106">Serviços base do TPM</span><span class="sxs-lookup"><span data-stu-id="fddea-106">TPM Base Services</span></span>

## <a name="purpose"></a><span data-ttu-id="fddea-107">Finalidade</span><span class="sxs-lookup"><span data-stu-id="fddea-107">Purpose</span></span>

<span data-ttu-id="fddea-108">O recurso TBS (serviços base) do Trusted Platform Module (TPM) centraliza o acesso do TPM entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fddea-108">The Trusted Platform Module (TPM) Base Services (TBS) feature centralizes TPM access across applications.</span></span>

<span data-ttu-id="fddea-109">O recurso TBS é executado como um serviço de sistema no Windows Server 2008, no Windows Vista ou em sistemas operacionais mais recentes.</span><span class="sxs-lookup"><span data-stu-id="fddea-109">The TBS feature runs as a system service in Windows Server 2008, Windows Vista, or newer operating systems.</span></span> <span data-ttu-id="fddea-110">Ele fornece serviços como uma API exposta por meio de chamadas de procedimento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="fddea-110">It provides services as an API exposed through remote procedure calls (RPC).</span></span> <span data-ttu-id="fddea-111">O recurso TBS usa prioridades especificadas chamando aplicativos para agendar de acordo com o acesso do TPM.</span><span class="sxs-lookup"><span data-stu-id="fddea-111">The TBS feature uses priorities specified by calling applications to cooperatively schedule TPM access.</span></span>

> [!Note]
>
> <span data-ttu-id="fddea-112">O TPM pode ser usado para operações de armazenamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="fddea-112">The TPM can be used for key storage operations.</span></span> <span data-ttu-id="fddea-113">No entanto, os desenvolvedores são incentivados a usar as [principais APIs de armazenamento](/windows/desktop/SecCNG/key-storage-and-retrieval) para esses cenários.</span><span class="sxs-lookup"><span data-stu-id="fddea-113">However, developers are encouraged to use the [Key Storage APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) for these scenarios instead.</span></span> <span data-ttu-id="fddea-114">As APIs de armazenamento de chaves fornecem a funcionalidade para criar, assinar ou criptografar e manter chaves criptográficas, e elas são de nível superior e mais fáceis de usar do que os TBS para esses cenários de destino.</span><span class="sxs-lookup"><span data-stu-id="fddea-114">The Key Storage APIs provide the functionality to create, sign or encrypt with, and persist cryptographic keys, and they are higher-level and easier to use than the TBS for these targeted scenarios.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="fddea-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="fddea-115">Developer audience</span></span>

<span data-ttu-id="fddea-116">O TBS destina-se ao uso por desenvolvedores de aplicativos baseados nos sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="fddea-116">TBS is intended for use by developers of applications based on the Windows operating systems.</span></span> <span data-ttu-id="fddea-117">Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++ e o ambiente de programação do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fddea-117">Developers should be familiar with the C and C++ programming languages and the Microsoft Windows programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fddea-118">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="fddea-118">Run-time requirements</span></span>

<span data-ttu-id="fddea-119">O recurso TBS requer pelo menos o sistema operacional Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fddea-119">The TBS feature requires at least Windows Server 2008 or Windows Vista operating system.</span></span> <span data-ttu-id="fddea-120">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="fddea-120">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fddea-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fddea-121">In this section</span></span>



| <span data-ttu-id="fddea-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="fddea-122">Topic</span></span>                                         | <span data-ttu-id="fddea-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="fddea-123">Description</span></span>                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="fddea-124">Sobre TBS</span><span class="sxs-lookup"><span data-stu-id="fddea-124">About TBS</span></span>](about-tbs.md)<br/>         | <span data-ttu-id="fddea-125">Conceitos principais e uma exibição de alto nível do recurso TBS.</span><span class="sxs-lookup"><span data-stu-id="fddea-125">Key concepts and a high-level view of the TBS feature.</span></span><br/>               |
| [<span data-ttu-id="fddea-126">Usando TBS</span><span class="sxs-lookup"><span data-stu-id="fddea-126">Using TBS</span></span>](using-tbs.md)<br/>         | <span data-ttu-id="fddea-127">Processos e procedimentos TBS para usar a API TBS.</span><span class="sxs-lookup"><span data-stu-id="fddea-127">TBS processes and procedures for using the TBS API.</span></span><br/>                  |
| [<span data-ttu-id="fddea-128">Referência de TBS</span><span class="sxs-lookup"><span data-stu-id="fddea-128">TBS Reference</span></span>](tbs-reference.md)<br/> | <span data-ttu-id="fddea-129">Documentação sobre as funções, estruturas e códigos de retorno do TBS.</span><span class="sxs-lookup"><span data-stu-id="fddea-129">Documentation about the TBS functions, structures, and return codes.</span></span><br/> |



 

 

