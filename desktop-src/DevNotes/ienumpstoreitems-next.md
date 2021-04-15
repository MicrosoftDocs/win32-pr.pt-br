---
description: Obtém o próximo número especificado de nomes de item de dados na sequência de enumeração.
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: 'Método IEnumPStoreItems:: Next (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 967f2f84553b87965d5b2c92d99e347cb259264b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747461"
---
# <a name="ienumpstoreitemsnext-method"></a><span data-ttu-id="6ebfa-103">Método IEnumPStoreItems:: Next</span><span class="sxs-lookup"><span data-stu-id="6ebfa-103">IEnumPStoreItems::Next method</span></span>

<span data-ttu-id="6ebfa-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6ebfa-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6ebfa-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6ebfa-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6ebfa-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6ebfa-108">Obtém o próximo número especificado de nomes de item de dados na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-108">Gets the next specified number of data item names in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ebfa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ebfa-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="6ebfa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ebfa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ebfa-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ebfa-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ebfa-112">O número de itens de dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-112">The number of data items requested.</span></span>

</dd> <dt>

<span data-ttu-id="6ebfa-113">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6ebfa-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ebfa-114">Um ponteiro para uma cadeia de caracteres na qual retornar o nome do item de dados.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-114">A pointer to a string in which to return the data item name.</span></span>

</dd> <dt>

<span data-ttu-id="6ebfa-115">*pceltFetched* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6ebfa-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ebfa-116">Um ponteiro para o número de nomes de item de dados realmente fornecidos.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-116">A pointer to the number of data item names actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ebfa-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ebfa-117">Return value</span></span>

<span data-ttu-id="6ebfa-118">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ebfa-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebfa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ebfa-119">Requirements</span></span>



| <span data-ttu-id="6ebfa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ebfa-120">Requirement</span></span> | <span data-ttu-id="6ebfa-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6ebfa-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebfa-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ebfa-122">Header</span></span><br/> | <dl> <span data-ttu-id="6ebfa-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ebfa-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6ebfa-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6ebfa-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="6ebfa-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ebfa-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ebfa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ebfa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebfa-127">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="6ebfa-127">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
