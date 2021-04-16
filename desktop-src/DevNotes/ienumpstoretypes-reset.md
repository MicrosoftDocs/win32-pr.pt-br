---
description: Redefine para o início da sequência de enumeração.
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
ms.openlocfilehash: 60aeb1f68bcbf18e903472fa736b5714076dfbfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750133"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="1abd2-103">Método IEnumPStoreTypes:: Reset</span><span class="sxs-lookup"><span data-stu-id="1abd2-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="1abd2-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1abd2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="1abd2-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1abd2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="1abd2-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="1abd2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="1abd2-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="1abd2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="1abd2-108">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="1abd2-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abd2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1abd2-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="1abd2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1abd2-110">Parameters</span></span>

<span data-ttu-id="1abd2-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1abd2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1abd2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1abd2-112">Return value</span></span>

<span data-ttu-id="1abd2-113">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1abd2-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1abd2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1abd2-114">Requirements</span></span>



| <span data-ttu-id="1abd2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1abd2-115">Requirement</span></span> | <span data-ttu-id="1abd2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1abd2-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1abd2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1abd2-117">Header</span></span><br/> | <dl> <span data-ttu-id="1abd2-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="1abd2-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="1abd2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1abd2-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="1abd2-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1abd2-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1abd2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1abd2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abd2-122">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="1abd2-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
