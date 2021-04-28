---
description: Interface IEnumPStoreTypes – fornece métodos de enumeração de padrão COM para a interface IPStore.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interface IEnumPStoreTypes (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089354"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="221d3-103">Interface IEnumPStoreTypes</span><span class="sxs-lookup"><span data-stu-id="221d3-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="221d3-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="221d3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="221d3-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="221d3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="221d3-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="221d3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="221d3-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="221d3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="221d3-108">Fornece métodos de enumeração de padrão COM para a interface [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="221d3-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="221d3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="221d3-109">Members</span></span>

<span data-ttu-id="221d3-110">A interface **IEnumPStoreTypes** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="221d3-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="221d3-111">**IEnumPStoreTypes** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="221d3-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="221d3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="221d3-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="221d3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="221d3-113">Methods</span></span>

<span data-ttu-id="221d3-114">A interface **IEnumPStoreTypes** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="221d3-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="221d3-115">Método</span><span class="sxs-lookup"><span data-stu-id="221d3-115">Method</span></span>                                  | <span data-ttu-id="221d3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="221d3-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="221d3-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="221d3-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="221d3-118">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="221d3-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="221d3-119">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="221d3-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="221d3-120">Obtém o próximo tipo de provedor especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="221d3-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="221d3-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="221d3-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="221d3-122">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="221d3-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="221d3-123">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="221d3-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="221d3-124">Ignora o tipo de provedor especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="221d3-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="221d3-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="221d3-125">Remarks</span></span>

<span data-ttu-id="221d3-126">O objeto enumerador deve ser liberado quando não estiver mais sendo usado.</span><span class="sxs-lookup"><span data-stu-id="221d3-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="221d3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="221d3-127">Requirements</span></span>



| <span data-ttu-id="221d3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="221d3-128">Requirement</span></span> | <span data-ttu-id="221d3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="221d3-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="221d3-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="221d3-130">Header</span></span><br/> | <dl> <span data-ttu-id="221d3-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="221d3-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="221d3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="221d3-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="221d3-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="221d3-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
