---
description: Fornece acesso ao contexto de um objeto de cadeia capicor. Esse contexto permite que a cadeia de confiança do certificado capicor seja usada em outras derivações de CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interface IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787455"
---
# <a name="ichaincontext-interface"></a><span data-ttu-id="474b5-104">Interface IChainContext</span><span class="sxs-lookup"><span data-stu-id="474b5-104">IChainContext interface</span></span>

<span data-ttu-id="474b5-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="474b5-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="474b5-106">A interface **IChainContext** fornece acesso ao contexto de um objeto de [**cadeia**](chain.md) capicor.</span><span class="sxs-lookup"><span data-stu-id="474b5-106">The **IChainContext** interface provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="474b5-107">Esse contexto permite que a cadeia de confiança do certificado capicor seja usada em outras derivações de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="474b5-107">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="474b5-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="474b5-108">When to use</span></span>

<span data-ttu-id="474b5-109">Use essa interface quando precisar usar um objeto de [**cadeia**](chain.md) capicor em outra derivação de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="474b5-109">Use this interface when you need to use a CAPICOM [**Chain**](chain.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="474b5-110">Membros</span><span class="sxs-lookup"><span data-stu-id="474b5-110">Members</span></span>

<span data-ttu-id="474b5-111">A interface **IChainContext** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="474b5-111">The **IChainContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="474b5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="474b5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="474b5-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="474b5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="474b5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="474b5-114">Methods</span></span>

<span data-ttu-id="474b5-115">A interface **IChainContext** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="474b5-115">The **IChainContext** interface has these methods.</span></span>



| <span data-ttu-id="474b5-116">Método</span><span class="sxs-lookup"><span data-stu-id="474b5-116">Method</span></span>                                           | <span data-ttu-id="474b5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="474b5-117">Description</span></span>                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="474b5-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="474b5-118">**FreeContext**</span></span>](ichaincontext-freecontext.md) | <span data-ttu-id="474b5-119">Libera um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="474b5-119">Releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="474b5-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="474b5-120">Properties</span></span>

<span data-ttu-id="474b5-121">A interface **IChainContext** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="474b5-121">The **IChainContext** interface has these properties.</span></span>



| <span data-ttu-id="474b5-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="474b5-122">Property</span></span>                                                      | <span data-ttu-id="474b5-123">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="474b5-123">Access type</span></span>           | <span data-ttu-id="474b5-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="474b5-124">Description</span></span>                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="474b5-125">**ChainContext**</span><span class="sxs-lookup"><span data-stu-id="474b5-125">**ChainContext**</span></span>](ichaincontext-chaincontext.md)<br/> | <span data-ttu-id="474b5-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="474b5-126">Read/write</span></span><br/> | <span data-ttu-id="474b5-127">Define ou recupera o \_ \_ contexto de cadeia de PCCERT de um certificado.</span><span class="sxs-lookup"><span data-stu-id="474b5-127">Sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="474b5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="474b5-128">Requirements</span></span>



| <span data-ttu-id="474b5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="474b5-129">Requirement</span></span> | <span data-ttu-id="474b5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="474b5-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="474b5-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="474b5-131">Redistributable</span></span><br/> | <span data-ttu-id="474b5-132">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="474b5-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="474b5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="474b5-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="474b5-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="474b5-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




