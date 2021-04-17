---
description: Obtém o próximo número especificado de provedores na sequência de enumeração.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'Método IEnumPStoreProviders:: Next (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f468d29682c4e3767d4d8fe7d59e60976f103484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748080"
---
# <a name="ienumpstoreprovidersnext-method"></a><span data-ttu-id="f8dea-103">Método IEnumPStoreProviders:: Next</span><span class="sxs-lookup"><span data-stu-id="f8dea-103">IEnumPStoreProviders::Next method</span></span>

<span data-ttu-id="f8dea-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8dea-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f8dea-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f8dea-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f8dea-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="f8dea-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f8dea-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f8dea-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f8dea-108">Obtém o próximo número especificado de provedores na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="f8dea-108">Gets the next specified number of providers in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8dea-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8dea-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="f8dea-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8dea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8dea-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8dea-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dea-112">O número de tipos de provedor solicitado.</span><span class="sxs-lookup"><span data-stu-id="f8dea-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="f8dea-113">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f8dea-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dea-114">Um ponteiro para uma cadeia de caracteres na qual retornar o nome do tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="f8dea-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="f8dea-115">*pceltFetched* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f8dea-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dea-116">Um ponteiro para o número de tipos de provedor que foi realmente fornecido.</span><span class="sxs-lookup"><span data-stu-id="f8dea-116">A pointer to the number of provider types that was actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8dea-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8dea-117">Return value</span></span>

<span data-ttu-id="f8dea-118">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8dea-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8dea-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8dea-119">Requirements</span></span>



| <span data-ttu-id="f8dea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8dea-120">Requirement</span></span> | <span data-ttu-id="f8dea-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f8dea-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8dea-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8dea-122">Header</span></span><br/> | <dl> <span data-ttu-id="f8dea-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8dea-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="f8dea-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f8dea-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="f8dea-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8dea-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8dea-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8dea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8dea-127">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="f8dea-127">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
