---
description: Representa uma propriedade estendida da Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Objeto Extended
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778686"
---
# <a name="extendedproperty-object"></a><span data-ttu-id="ae6e6-103">Objeto Extended</span><span class="sxs-lookup"><span data-stu-id="ae6e6-103">ExtendedProperty object</span></span>

<span data-ttu-id="ae6e6-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ae6e6-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="ae6e6-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae6e6-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="ae6e6-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="ae6e6-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="ae6e6-108">O objeto **Extended** representa uma propriedade estendida da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-108">The **ExtendedProperty** object represents a Microsoft-extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ae6e6-109">Quando usar</span><span class="sxs-lookup"><span data-stu-id="ae6e6-109">When to use</span></span>

<span data-ttu-id="ae6e6-110">O objeto **Extended** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="ae6e6-110">The **ExtendedProperty** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="ae6e6-111">Defina ou recupere o tipo da propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-111">Set or retrieve the type of the extended property.</span></span>
-   <span data-ttu-id="ae6e6-112">Defina ou recupere o tipo de codificação usado para codificar a propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-112">Set or retrieve the type of encoding used to encode the extended property.</span></span>

## <a name="members"></a><span data-ttu-id="ae6e6-113">Membros</span><span class="sxs-lookup"><span data-stu-id="ae6e6-113">Members</span></span>

<span data-ttu-id="ae6e6-114">O objeto **Extended** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ae6e6-114">The **ExtendedProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="ae6e6-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae6e6-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae6e6-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae6e6-116">Properties</span></span>

<span data-ttu-id="ae6e6-117">O objeto **Extended** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-117">The **ExtendedProperty** object has these properties.</span></span>



| <span data-ttu-id="ae6e6-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ae6e6-118">Property</span></span>                                             | <span data-ttu-id="ae6e6-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="ae6e6-119">Access type</span></span>           | <span data-ttu-id="ae6e6-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae6e6-120">Description</span></span>                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae6e6-121">**PropID**</span><span class="sxs-lookup"><span data-stu-id="ae6e6-121">**PropID**</span></span>](extendedproperty-propid.md)<br/> | <span data-ttu-id="ae6e6-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ae6e6-122">Read/write</span></span><br/> | <span data-ttu-id="ae6e6-123">Um valor da enumeração [**\_ Propid de CAPICOM**](capicom-propid.md) que define ou recupera o tipo de propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-123">A value of the [**CAPICOM\_PROPID**](capicom-propid.md) enumeration that sets or retrieves the type of extended property.</span></span><br/> <span data-ttu-id="ae6e6-124">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-124">This is the default property.</span></span><br/> |
| [<span data-ttu-id="ae6e6-125">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae6e6-125">**Value**</span></span>](extendedproperty-value.md)<br/>   | <span data-ttu-id="ae6e6-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ae6e6-126">Read/write</span></span><br/> | <span data-ttu-id="ae6e6-127">Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que define ou recupera os dados da propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-127">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that sets or retrieves the extended property data.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="ae6e6-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae6e6-128">Remarks</span></span>

<span data-ttu-id="ae6e6-129">O objeto **Extended** é usado pela coleção [**ExtendedProperties**](extendedproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6e6-129">The **ExtendedProperty** object is used by the [**ExtendedProperties**](extendedproperties.md) collection.</span></span>

<span data-ttu-id="ae6e6-130">O objeto **Extended** pode ser criado e não é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-130">The **ExtendedProperty** object can be created, and it is not safe for scripting.</span></span> <span data-ttu-id="ae6e6-131">O ProgID para o objeto **Extended** é CAPICOM. Extended. 1.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-131">The ProgID for the **ExtendedProperty** object is CAPICOM.ExtendedProperty.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6e6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6e6-132">Requirements</span></span>



| <span data-ttu-id="ae6e6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6e6-133">Requirement</span></span> | <span data-ttu-id="ae6e6-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ae6e6-134">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6e6-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ae6e6-135">End of client support</span></span><br/> | <span data-ttu-id="ae6e6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae6e6-136">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ae6e6-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ae6e6-137">End of server support</span></span><br/> | <span data-ttu-id="ae6e6-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae6e6-138">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ae6e6-139">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ae6e6-139">Redistributable</span></span><br/>       | <span data-ttu-id="ae6e6-140">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ae6e6-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ae6e6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ae6e6-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ae6e6-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6e6-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
