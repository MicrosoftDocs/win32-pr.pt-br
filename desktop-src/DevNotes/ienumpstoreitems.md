---
description: Fornece os métodos de enumeração COM padrão para a interface IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interface IEnumPStoreItems (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749286"
---
# <a name="ienumpstoreitems-interface"></a><span data-ttu-id="66f65-103">Interface IEnumPStoreItems</span><span class="sxs-lookup"><span data-stu-id="66f65-103">IEnumPStoreItems interface</span></span>

<span data-ttu-id="66f65-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="66f65-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="66f65-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="66f65-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="66f65-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="66f65-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="66f65-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="66f65-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="66f65-108">Fornece os métodos de enumeração COM padrão para a interface [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="66f65-108">Provides the COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="66f65-109">Membros</span><span class="sxs-lookup"><span data-stu-id="66f65-109">Members</span></span>

<span data-ttu-id="66f65-110">A interface **IEnumPStoreItems** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="66f65-110">The **IEnumPStoreItems** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="66f65-111">**IEnumPStoreItems** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="66f65-111">**IEnumPStoreItems** also has these types of members:</span></span>

-   [<span data-ttu-id="66f65-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="66f65-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66f65-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="66f65-113">Methods</span></span>

<span data-ttu-id="66f65-114">A interface **IEnumPStoreItems** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="66f65-114">The **IEnumPStoreItems** interface has these methods.</span></span>



| <span data-ttu-id="66f65-115">Método</span><span class="sxs-lookup"><span data-stu-id="66f65-115">Method</span></span>                                  | <span data-ttu-id="66f65-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="66f65-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66f65-117">**8i**</span><span class="sxs-lookup"><span data-stu-id="66f65-117">**Clone**</span></span>](ienumpstoreitems-clone.md) | <span data-ttu-id="66f65-118">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="66f65-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="66f65-119">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="66f65-119">**Next**</span></span>](ienumpstoreitems-next.md)   | <span data-ttu-id="66f65-120">Obtém o próximo item de dados especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="66f65-120">Gets the next specified data item in the enumeration sequence.</span></span><br/>                          |
| [<span data-ttu-id="66f65-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="66f65-121">**Reset**</span></span>](ienumpstoreitems-reset.md) | <span data-ttu-id="66f65-122">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="66f65-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="66f65-123">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="66f65-123">**Skip**</span></span>](ienumpstoreitems-skip.md)   | <span data-ttu-id="66f65-124">Ignora o item de dados especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="66f65-124">Skips the specified data item in the enumeration sequence.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="66f65-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="66f65-125">Remarks</span></span>

<span data-ttu-id="66f65-126">É necessário liberar cada item depois de enumera-lo.</span><span class="sxs-lookup"><span data-stu-id="66f65-126">It is necessary to free each item after enumerating it.</span></span> <span data-ttu-id="66f65-127">O objeto Enumerator também deve ser liberado quando não estiver mais sendo usado.</span><span class="sxs-lookup"><span data-stu-id="66f65-127">The enumerator object must also be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f65-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f65-128">Requirements</span></span>



| <span data-ttu-id="66f65-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f65-129">Requirement</span></span> | <span data-ttu-id="66f65-130">Valor</span><span class="sxs-lookup"><span data-stu-id="66f65-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66f65-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f65-131">Header</span></span><br/> | <dl> <span data-ttu-id="66f65-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f65-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="66f65-133">DLL</span><span class="sxs-lookup"><span data-stu-id="66f65-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="66f65-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66f65-134"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
