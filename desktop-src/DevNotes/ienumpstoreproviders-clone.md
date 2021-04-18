---
description: Cria outro enumerador que contém o mesmo estado de enumeração do atual.
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'Método IEnumPStoreProviders:: clone (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdd7825a44dcea672eff24a15126921f0426a986
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750161"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="975ec-103">Método IEnumPStoreProviders:: clone</span><span class="sxs-lookup"><span data-stu-id="975ec-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="975ec-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="975ec-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="975ec-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="975ec-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="975ec-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="975ec-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="975ec-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="975ec-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="975ec-108">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="975ec-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="975ec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="975ec-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="975ec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="975ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="975ec-111">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="975ec-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="975ec-112">Um ponteiro para um ponteiro [**IEnumPStoreProviders**](ienumpstoreproviders.md) .</span><span class="sxs-lookup"><span data-stu-id="975ec-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="975ec-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="975ec-113">Return value</span></span>

<span data-ttu-id="975ec-114">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="975ec-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="975ec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="975ec-115">Requirements</span></span>



| <span data-ttu-id="975ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="975ec-116">Requirement</span></span> | <span data-ttu-id="975ec-117">Valor</span><span class="sxs-lookup"><span data-stu-id="975ec-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="975ec-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="975ec-118">Header</span></span><br/> | <dl> <span data-ttu-id="975ec-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="975ec-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="975ec-120">DLL</span><span class="sxs-lookup"><span data-stu-id="975ec-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="975ec-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="975ec-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="975ec-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="975ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="975ec-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="975ec-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
