---
description: Obtém o próximo número especificado de tipos de provedor na sequência de enumeração.
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'Método IEnumPStoreTypes:: Next (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 18981053de897b75d1febdc75e138e6561e65bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747626"
---
# <a name="ienumpstoretypesnext-method"></a><span data-ttu-id="45b17-103">Método IEnumPStoreTypes:: Next</span><span class="sxs-lookup"><span data-stu-id="45b17-103">IEnumPStoreTypes::Next method</span></span>

<span data-ttu-id="45b17-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="45b17-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="45b17-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="45b17-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="45b17-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="45b17-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="45b17-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="45b17-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="45b17-108">Obtém o próximo número especificado de tipos de provedor na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="45b17-108">Gets the next specified number of provider types in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b17-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45b17-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="45b17-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45b17-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b17-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45b17-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b17-112">O número de tipos de provedor solicitado.</span><span class="sxs-lookup"><span data-stu-id="45b17-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="45b17-113">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="45b17-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45b17-114">Um ponteiro para uma cadeia de caracteres na qual retornar o nome do tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="45b17-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="45b17-115">*pceltFetched* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="45b17-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45b17-116">Um ponteiro para o número de tipos de provedor realmente fornecidos.</span><span class="sxs-lookup"><span data-stu-id="45b17-116">A pointer to the number of provider types actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b17-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45b17-117">Return value</span></span>

<span data-ttu-id="45b17-118">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45b17-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b17-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b17-119">Requirements</span></span>



| <span data-ttu-id="45b17-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b17-120">Requirement</span></span> | <span data-ttu-id="45b17-121">Valor</span><span class="sxs-lookup"><span data-stu-id="45b17-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45b17-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45b17-122">Header</span></span><br/> | <dl> <span data-ttu-id="45b17-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b17-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="45b17-124">DLL</span><span class="sxs-lookup"><span data-stu-id="45b17-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="45b17-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b17-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b17-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="45b17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b17-127">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="45b17-127">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
