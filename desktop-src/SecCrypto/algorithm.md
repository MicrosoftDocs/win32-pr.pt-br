---
description: Especifica o algoritmo usado para as operações de assinatura, enveloping e criptografia.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Objeto Algorithm (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764626"
---
# <a name="algorithm-object"></a><span data-ttu-id="c6793-103">Objeto de algoritmo</span><span class="sxs-lookup"><span data-stu-id="c6793-103">Algorithm object</span></span>

<span data-ttu-id="c6793-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6793-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="c6793-105">Em vez disso, use a [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="c6793-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="c6793-106">O objeto **Algorithm** especifica o algoritmo usado para as operações de assinatura, enveloping e criptografia.</span><span class="sxs-lookup"><span data-stu-id="c6793-106">The **Algorithm** object specifies the algorithm used for signing, enveloping, and encrypting operations.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c6793-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="c6793-107">When to use</span></span>

<span data-ttu-id="c6793-108">O objeto de **algoritmo** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c6793-108">The **Algorithm** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="c6793-109">Defina ou recupere o algoritmo a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c6793-109">Set or retrieve the algorithm to be used.</span></span>
-   <span data-ttu-id="c6793-110">Definir ou recuperar o comprimento da chave.</span><span class="sxs-lookup"><span data-stu-id="c6793-110">Set or retrieve the key length.</span></span>

> [!Note]  
> <span data-ttu-id="c6793-111">O CAPICOM tenta usar o CSP (provedor de serviços de criptografia) padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6793-111">CAPICOM attempts to use the system default cryptographic service provider (CSP).</span></span> <span data-ttu-id="c6793-112">Se esse CSP não puder fornecer o algoritmo ou o comprimento de chave solicitado, o CAPICOM procura um CSP fornecido pela Microsoft que possa lidar com o algoritmo e o comprimento de chave solicitados, nesta ordem de disponibilidade: provedor criptográfico aprimorado da Microsoft, provedor de criptografia forte da Microsoft, provedor criptográfico base da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6793-112">If that CSP cannot provide the requested algorithm or key length, CAPICOM searches for an available Microsoft-provided CSP that can handle the requested algorithm and key length, in this order of availability: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span></span>

 

## <a name="members"></a><span data-ttu-id="c6793-113">Membros</span><span class="sxs-lookup"><span data-stu-id="c6793-113">Members</span></span>

<span data-ttu-id="c6793-114">O objeto de **algoritmo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c6793-114">The **Algorithm** object has these types of members:</span></span>

-   [<span data-ttu-id="c6793-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6793-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6793-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6793-116">Properties</span></span>

<span data-ttu-id="c6793-117">O objeto de **algoritmo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c6793-117">The **Algorithm** object has these properties.</span></span>



| <span data-ttu-id="c6793-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c6793-118">Property</span></span>                                            | <span data-ttu-id="c6793-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c6793-119">Access type</span></span>           | <span data-ttu-id="c6793-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6793-120">Description</span></span>                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6793-121">**KeyLength da**</span><span class="sxs-lookup"><span data-stu-id="c6793-121">**KeyLength**</span></span>](algorithm-keylength.md)<br/> | <span data-ttu-id="c6793-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c6793-122">Read/write</span></span><br/> | <span data-ttu-id="c6793-123">Define ou recupera o comprimento da chave.</span><span class="sxs-lookup"><span data-stu-id="c6793-123">Sets or retrieves the length of the key.</span></span><br/>                                                                               |
| [<span data-ttu-id="c6793-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c6793-124">**Name**</span></span>](algorithm-name.md)<br/>           | <span data-ttu-id="c6793-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c6793-125">Read/write</span></span><br/> | <span data-ttu-id="c6793-126">Define ou recupera o algoritmo usado para as operações de assinatura, enveloping e criptografia.</span><span class="sxs-lookup"><span data-stu-id="c6793-126">Sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="c6793-127">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="c6793-127">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6793-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6793-128">Remarks</span></span>

<span data-ttu-id="c6793-129">Não é possível criar o objeto de **algoritmo** .</span><span class="sxs-lookup"><span data-stu-id="c6793-129">The **Algorithm** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6793-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6793-130">Requirements</span></span>



| <span data-ttu-id="c6793-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6793-131">Requirement</span></span> | <span data-ttu-id="c6793-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c6793-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6793-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c6793-133">End of client support</span></span><br/> | <span data-ttu-id="c6793-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6793-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c6793-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c6793-135">End of server support</span></span><br/> | <span data-ttu-id="c6793-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6793-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c6793-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c6793-137">Redistributable</span></span><br/>       | <span data-ttu-id="c6793-138">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6793-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c6793-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6793-139">Header</span></span><br/>                | <dl> <span data-ttu-id="c6793-140"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6793-140"><dt>Capicom.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6793-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c6793-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c6793-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6793-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6793-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6793-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6793-144">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="c6793-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
