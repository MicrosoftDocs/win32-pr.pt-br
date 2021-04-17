---
description: Representa um único atributo autenticado.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Objeto Attribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811804"
---
# <a name="attribute-object"></a><span data-ttu-id="3a4f5-103">Objeto Attribute</span><span class="sxs-lookup"><span data-stu-id="3a4f5-103">Attribute object</span></span>

<span data-ttu-id="3a4f5-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="3a4f5-105">Em vez disso, use a [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="3a4f5-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="3a4f5-106">O objeto de **atributo** representa um único atributo autenticado.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-106">The **Attribute** object represents a single authenticated attribute.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3a4f5-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="3a4f5-107">When to use</span></span>

<span data-ttu-id="3a4f5-108">O objeto **Attribute** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="3a4f5-108">The **Attribute** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="3a4f5-109">Defina ou recupere o nome do CAPICOM do atributo.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-109">Set or retrieve the CAPICOM name of the attribute.</span></span>
-   <span data-ttu-id="3a4f5-110">Defina ou recupere o valor do atributo, como a hora de assinatura, o nome do documento assinado ou uma descrição do documento assinado.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-110">Set or retrieve the value of the attribute, such as signing time, the name of the document signed, or a description of the document signed.</span></span>

## <a name="members"></a><span data-ttu-id="3a4f5-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3a4f5-111">Members</span></span>

<span data-ttu-id="3a4f5-112">O objeto de **atributo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3a4f5-112">The **Attribute** object has these types of members:</span></span>

-   [<span data-ttu-id="3a4f5-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a4f5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a4f5-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a4f5-114">Properties</span></span>

<span data-ttu-id="3a4f5-115">O objeto **Attribute** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-115">The **Attribute** object has these properties.</span></span>



| <span data-ttu-id="3a4f5-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3a4f5-116">Property</span></span>                                    | <span data-ttu-id="3a4f5-117">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="3a4f5-117">Access type</span></span>           | <span data-ttu-id="3a4f5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a4f5-118">Description</span></span>                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a4f5-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3a4f5-119">**Name**</span></span>](attribute-name.md)<br/>   | <span data-ttu-id="3a4f5-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3a4f5-120">Read/write</span></span><br/> | <span data-ttu-id="3a4f5-121">Define ou recupera o nome do CAPICOM do atributo.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-121">Sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="3a4f5-122">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-122">This is the default property.</span></span><br/> |
| [<span data-ttu-id="3a4f5-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3a4f5-123">**Value**</span></span>](attribute-value.md)<br/> | <span data-ttu-id="3a4f5-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3a4f5-124">Read/write</span></span><br/> | <span data-ttu-id="3a4f5-125">Define ou recupera o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-125">Sets or retrieves the value of the attribute.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="3a4f5-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a4f5-126">Remarks</span></span>

<span data-ttu-id="3a4f5-127">O objeto **Attribute** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-127">The **Attribute** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="3a4f5-128">O ProgID do objeto de **atributo** é CAPICOM. Atributo. 1.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-128">The ProgID for the **Attribute** object is CAPICOM.Attribute.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4f5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a4f5-129">Requirements</span></span>



| <span data-ttu-id="3a4f5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a4f5-130">Requirement</span></span> | <span data-ttu-id="3a4f5-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3a4f5-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4f5-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3a4f5-132">End of client support</span></span><br/> | <span data-ttu-id="3a4f5-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a4f5-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3a4f5-134">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3a4f5-134">End of server support</span></span><br/> | <span data-ttu-id="3a4f5-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a4f5-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3a4f5-136">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3a4f5-136">Redistributable</span></span><br/>       | <span data-ttu-id="3a4f5-137">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a4f5-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3a4f5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3a4f5-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3a4f5-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a4f5-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4f5-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a4f5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4f5-141">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="3a4f5-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
