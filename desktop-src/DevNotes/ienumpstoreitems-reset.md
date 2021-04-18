---
description: Redefine para o início da sequência de enumeração fornecida.
ms.assetid: add91f5d-3f84-4069-93c0-9380a3935b85
title: 'Método IEnumPStoreItems:: Reset (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d5b05c23ba40ab647b2c4b3bb552f92ee34e12c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756407"
---
# <a name="ienumpstoreitemsreset-method"></a><span data-ttu-id="d54b9-103">Método IEnumPStoreItems:: Reset</span><span class="sxs-lookup"><span data-stu-id="d54b9-103">IEnumPStoreItems::Reset method</span></span>

<span data-ttu-id="d54b9-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d54b9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d54b9-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d54b9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d54b9-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="d54b9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d54b9-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d54b9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d54b9-108">Redefine para o início da sequência de enumeração fornecida.</span><span class="sxs-lookup"><span data-stu-id="d54b9-108">Resets to the beginning of the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="d54b9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d54b9-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="d54b9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d54b9-110">Parameters</span></span>

<span data-ttu-id="d54b9-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d54b9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d54b9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d54b9-112">Return value</span></span>

<span data-ttu-id="d54b9-113">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d54b9-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d54b9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d54b9-114">Requirements</span></span>



| <span data-ttu-id="d54b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d54b9-115">Requirement</span></span> | <span data-ttu-id="d54b9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d54b9-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d54b9-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d54b9-117">Header</span></span><br/> | <dl> <span data-ttu-id="d54b9-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d54b9-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d54b9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d54b9-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="d54b9-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d54b9-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d54b9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d54b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54b9-122">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="d54b9-122">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
