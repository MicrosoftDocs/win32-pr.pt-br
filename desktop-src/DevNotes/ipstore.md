---
description: Fornece métodos COM padrão para gerenciar itens de dados de armazenamento protegidos.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Interface IPStore (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751957"
---
# <a name="ipstore-interface"></a><span data-ttu-id="12ee8-103">Interface IPStore</span><span class="sxs-lookup"><span data-stu-id="12ee8-103">IPStore interface</span></span>

<span data-ttu-id="12ee8-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12ee8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="12ee8-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="12ee8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="12ee8-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="12ee8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="12ee8-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="12ee8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="12ee8-108">\[Essa interface pode ser alterada ou não estar disponível em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12ee8-108">\[This interface may be altered or unavailable in future versions of Windows.\]</span></span>

<span data-ttu-id="12ee8-109">Fornece métodos COM padrão para gerenciar itens de dados de armazenamento protegidos.</span><span class="sxs-lookup"><span data-stu-id="12ee8-109">Provides COM-standard methods to manage protected storage data items.</span></span> <span data-ttu-id="12ee8-110">O método [**PStoreCreateInstance**](pstorecreateinstance.md) retorna um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="12ee8-110">The [**PStoreCreateInstance**](pstorecreateinstance.md) method returns a pointer to this interface.</span></span>

## <a name="members"></a><span data-ttu-id="12ee8-111">Membros</span><span class="sxs-lookup"><span data-stu-id="12ee8-111">Members</span></span>

<span data-ttu-id="12ee8-112">A interface **IPStore** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="12ee8-112">The **IPStore** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="12ee8-113">**IPStore** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12ee8-113">**IPStore** also has these types of members:</span></span>

-   [<span data-ttu-id="12ee8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="12ee8-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="12ee8-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="12ee8-115">Methods</span></span>

<span data-ttu-id="12ee8-116">A interface **IPStore** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="12ee8-116">The **IPStore** interface has these methods.</span></span>



| <span data-ttu-id="12ee8-117">Método</span><span class="sxs-lookup"><span data-stu-id="12ee8-117">Method</span></span>                                                   | <span data-ttu-id="12ee8-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="12ee8-118">Description</span></span>                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12ee8-119">**CloseItem**</span><span class="sxs-lookup"><span data-stu-id="12ee8-119">**CloseItem**</span></span>](ipstore-closeitem.md)                   | <span data-ttu-id="12ee8-120">Fecha um item de dados especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-120">Closes a specified data item from protected storage.</span></span><br/>                                                       |
| [<span data-ttu-id="12ee8-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="12ee8-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)           | <span data-ttu-id="12ee8-122">Cria o subtipo especificado dentro do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="12ee8-122">Creates the specified subtype within the specified type.</span></span><br/>                                                   |
| [<span data-ttu-id="12ee8-123">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="12ee8-123">**CreateType**</span></span>](ipstore-createtype.md)                 | <span data-ttu-id="12ee8-124">Cria o tipo especificado com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="12ee8-124">Creates the specified type with the specified name.</span></span><br/>                                                        |
| [<span data-ttu-id="12ee8-125">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="12ee8-125">**DeleteItem**</span></span>](ipstore-deleteitem.md)                 | <span data-ttu-id="12ee8-126">Exclui o item especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-126">Deletes the specified item from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="12ee8-127">**DeleteSubtype**</span><span class="sxs-lookup"><span data-stu-id="12ee8-127">**DeleteSubtype**</span></span>](ipstore-deletesubtype.md)           | <span data-ttu-id="12ee8-128">Exclui o subtipo de item especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-128">Deletes the specified item subtype from the protected storage.</span></span><br/>                                             |
| [<span data-ttu-id="12ee8-129">**Excluirtype**</span><span class="sxs-lookup"><span data-stu-id="12ee8-129">**DeleteType**</span></span>](ipstore-deletetype.md)                 | <span data-ttu-id="12ee8-130">Exclui o tipo especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-130">Deletes the specified type from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="12ee8-131">**EnumItems**</span><span class="sxs-lookup"><span data-stu-id="12ee8-131">**EnumItems**</span></span>](ipstore-enumitems.md)                   | <span data-ttu-id="12ee8-132">Retorna o ponteiro de interface de um subtipo para enumerar itens no banco de dados de armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-132">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span><br/>        |
| [<span data-ttu-id="12ee8-133">**EnumSubtypes**</span><span class="sxs-lookup"><span data-stu-id="12ee8-133">**EnumSubtypes**</span></span>](ipstore-enumsubtypes.md)             | <span data-ttu-id="12ee8-134">Retorna uma interface para enumerar subtipos dos tipos atualmente registrados no banco de dados protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-134">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span><br/> |
| [<span data-ttu-id="12ee8-135">**EnumTypes**</span><span class="sxs-lookup"><span data-stu-id="12ee8-135">**EnumTypes**</span></span>](ipstore-enumtypes.md)                   | <span data-ttu-id="12ee8-136">Retorna uma interface para enumerar os tipos atualmente registrados no banco de dados protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-136">Returns an interface for enumerating the types currently registered in the protected database.</span></span><br/>             |
| [<span data-ttu-id="12ee8-137">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="12ee8-137">**GetInfo**</span></span>](ipstore-getinfo.md)                       | <span data-ttu-id="12ee8-138">Recupera informações sobre o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12ee8-138">Retrieves information about the storage provider.</span></span><br/>                                                          |
| [<span data-ttu-id="12ee8-139">**GetProvParam**</span><span class="sxs-lookup"><span data-stu-id="12ee8-139">**GetProvParam**</span></span>](ipstore-getprovparam.md)             | <span data-ttu-id="12ee8-140">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="12ee8-140">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="12ee8-141">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="12ee8-141">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)         | <span data-ttu-id="12ee8-142">Recupera informações associadas a um subtipo.</span><span class="sxs-lookup"><span data-stu-id="12ee8-142">Retrieves information associated with a subtype.</span></span><br/>                                                           |
| [<span data-ttu-id="12ee8-143">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="12ee8-143">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)               | <span data-ttu-id="12ee8-144">Recupera informações associadas a um tipo.</span><span class="sxs-lookup"><span data-stu-id="12ee8-144">Retrieves information associated with a type.</span></span><br/>                                                              |
| [<span data-ttu-id="12ee8-145">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="12ee8-145">**OpenItem**</span></span>](ipstore-openitem.md)                     | <span data-ttu-id="12ee8-146">Abre um item para vários acessos.</span><span class="sxs-lookup"><span data-stu-id="12ee8-146">Opens an item for multiple accesses.</span></span><br/>                                                                       |
| [<span data-ttu-id="12ee8-147">**ReadAccessRuleSet**</span><span class="sxs-lookup"><span data-stu-id="12ee8-147">**ReadAccessRuleSet**</span></span>](ipstore-readaccessruleset.md)   | <span data-ttu-id="12ee8-148">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="12ee8-148">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="12ee8-149">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="12ee8-149">**ReadItem**</span></span>](ipstore-readitem.md)                     | <span data-ttu-id="12ee8-150">Lê o item de dados especificado do armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-150">Reads the specified data item from protected storage.</span></span><br/>                                                      |
| [<span data-ttu-id="12ee8-151">**SetProvParam**</span><span class="sxs-lookup"><span data-stu-id="12ee8-151">**SetProvParam**</span></span>](ipstore-setprovparam.md)             | <span data-ttu-id="12ee8-152">Define as informações do parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="12ee8-152">Sets the specified parameter information.</span></span><br/>                                                                  |
| [<span data-ttu-id="12ee8-153">**WriteAccessRuleset**</span><span class="sxs-lookup"><span data-stu-id="12ee8-153">**WriteAccessRuleset**</span></span>](ipstore-writeaccessruleset.md) | <span data-ttu-id="12ee8-154">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="12ee8-154">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="12ee8-155">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="12ee8-155">**WriteItem**</span></span>](ipstore-writeitem.md)                   | <span data-ttu-id="12ee8-156">Grava um item de dados no armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="12ee8-156">Writes a data item to protected storage.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="12ee8-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ee8-157">Requirements</span></span>



| <span data-ttu-id="12ee8-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ee8-158">Requirement</span></span> | <span data-ttu-id="12ee8-159">Valor</span><span class="sxs-lookup"><span data-stu-id="12ee8-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12ee8-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12ee8-160">Header</span></span><br/> | <dl> <span data-ttu-id="12ee8-161"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="12ee8-161"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="12ee8-162">DLL</span><span class="sxs-lookup"><span data-stu-id="12ee8-162">DLL</span></span><br/>    | <dl> <span data-ttu-id="12ee8-163"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12ee8-163"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
