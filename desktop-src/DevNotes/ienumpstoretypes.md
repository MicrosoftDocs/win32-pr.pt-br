---
description: Fornece métodos de enumeração de padrão COM para a interface IPStore.
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
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748908"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="f63e6-103">Interface IEnumPStoreTypes</span><span class="sxs-lookup"><span data-stu-id="f63e6-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="f63e6-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f63e6-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f63e6-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f63e6-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f63e6-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="f63e6-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f63e6-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f63e6-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f63e6-108">Fornece métodos de enumeração de padrão COM para a interface [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="f63e6-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="f63e6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f63e6-109">Members</span></span>

<span data-ttu-id="f63e6-110">A interface **IEnumPStoreTypes** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f63e6-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f63e6-111">**IEnumPStoreTypes** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f63e6-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="f63e6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f63e6-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f63e6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f63e6-113">Methods</span></span>

<span data-ttu-id="f63e6-114">A interface **IEnumPStoreTypes** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f63e6-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="f63e6-115">Método</span><span class="sxs-lookup"><span data-stu-id="f63e6-115">Method</span></span>                                  | <span data-ttu-id="f63e6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f63e6-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f63e6-117">**8i**</span><span class="sxs-lookup"><span data-stu-id="f63e6-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="f63e6-118">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="f63e6-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="f63e6-119">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="f63e6-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="f63e6-120">Obtém o próximo tipo de provedor especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="f63e6-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="f63e6-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="f63e6-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="f63e6-122">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="f63e6-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="f63e6-123">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="f63e6-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="f63e6-124">Ignora o tipo de provedor especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="f63e6-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="f63e6-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f63e6-125">Remarks</span></span>

<span data-ttu-id="f63e6-126">O objeto enumerador deve ser liberado quando não estiver mais sendo usado.</span><span class="sxs-lookup"><span data-stu-id="f63e6-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63e6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f63e6-127">Requirements</span></span>



| <span data-ttu-id="f63e6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63e6-128">Requirement</span></span> | <span data-ttu-id="f63e6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f63e6-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f63e6-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f63e6-130">Header</span></span><br/> | <dl> <span data-ttu-id="f63e6-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f63e6-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="f63e6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f63e6-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="f63e6-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f63e6-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
