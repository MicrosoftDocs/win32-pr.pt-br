---
description: Interface IEnumPStoreProviders – fornece métodos de enumeração de padrão COM para a interface IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interface IEnumPStoreProviders (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089344"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="8326e-103">Interface IEnumPStoreProviders</span><span class="sxs-lookup"><span data-stu-id="8326e-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="8326e-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8326e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="8326e-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8326e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="8326e-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="8326e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="8326e-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="8326e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="8326e-108">Fornece métodos de enumeração de padrão COM para a interface [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="8326e-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="8326e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8326e-109">Members</span></span>

<span data-ttu-id="8326e-110">A interface **IEnumPStoreProviders** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8326e-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8326e-111">**IEnumPStoreProviders** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8326e-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="8326e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8326e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8326e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8326e-113">Methods</span></span>

<span data-ttu-id="8326e-114">A interface **IEnumPStoreProviders** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8326e-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="8326e-115">Método</span><span class="sxs-lookup"><span data-stu-id="8326e-115">Method</span></span>                                      | <span data-ttu-id="8326e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8326e-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8326e-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="8326e-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="8326e-118">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="8326e-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="8326e-119">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="8326e-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="8326e-120">Obtém o próximo provedor especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="8326e-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="8326e-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="8326e-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="8326e-122">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="8326e-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="8326e-123">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="8326e-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="8326e-124">Ignora o provedor especificado na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="8326e-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="8326e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8326e-125">Requirements</span></span>



| <span data-ttu-id="8326e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8326e-126">Requirement</span></span> | <span data-ttu-id="8326e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8326e-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8326e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8326e-128">Header</span></span><br/> | <dl> <span data-ttu-id="8326e-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="8326e-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="8326e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8326e-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="8326e-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8326e-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
