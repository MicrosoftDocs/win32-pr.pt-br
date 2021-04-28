---
description: 'Método IEnumPStoreTypes:: Reset – redefine para o início da sequência de enumeração.'
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: 'Método IEnumPStoreTypes:: Reset (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 55953a67d19ac94f792769974d860bae9b57f1ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089314"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="4b8db-103">Método IEnumPStoreTypes:: Reset</span><span class="sxs-lookup"><span data-stu-id="4b8db-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="4b8db-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b8db-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4b8db-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4b8db-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4b8db-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="4b8db-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4b8db-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4b8db-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4b8db-108">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="4b8db-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8db-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b8db-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="4b8db-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b8db-110">Parameters</span></span>

<span data-ttu-id="4b8db-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b8db-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b8db-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4b8db-112">Return value</span></span>

<span data-ttu-id="4b8db-113">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b8db-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8db-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b8db-114">Requirements</span></span>



| <span data-ttu-id="4b8db-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8db-115">Requirement</span></span> | <span data-ttu-id="4b8db-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4b8db-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8db-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b8db-117">Header</span></span><br/> | <dl> <span data-ttu-id="4b8db-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b8db-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4b8db-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8db-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="4b8db-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b8db-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b8db-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4b8db-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8db-122">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="4b8db-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
