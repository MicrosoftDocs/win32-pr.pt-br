---
description: Grava as regras de acesso para o tipo fornecido.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'Método IPStore:: WriteAccessRuleset (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7399ff800087720d65cb45e80ccab080a7df9baf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811247"
---
# <a name="ipstorewriteaccessruleset-method"></a><span data-ttu-id="5c94d-103">Método IPStore:: WriteAccessRuleset</span><span class="sxs-lookup"><span data-stu-id="5c94d-103">IPStore::WriteAccessRuleset method</span></span>

<span data-ttu-id="5c94d-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c94d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5c94d-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5c94d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5c94d-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="5c94d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5c94d-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5c94d-108">\[Este método não está implementado.\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="5c94d-109">Grava as regras de acesso para o tipo fornecido.</span><span class="sxs-lookup"><span data-stu-id="5c94d-109">Writes the access rules for the given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c94d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c94d-110">Syntax</span></span>


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5c94d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c94d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c94d-112">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c94d-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c94d-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c94d-114">*pType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c94d-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c94d-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c94d-116">*pSubtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c94d-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c94d-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c94d-118">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c94d-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c94d-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c94d-120">*pRules* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-120">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c94d-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c94d-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c94d-122">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c94d-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c94d-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5c94d-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c94d-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c94d-124">Return value</span></span>

<span data-ttu-id="5c94d-125">As chamadas para esse método sempre falharão.</span><span class="sxs-lookup"><span data-stu-id="5c94d-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c94d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c94d-126">Requirements</span></span>



| <span data-ttu-id="5c94d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c94d-127">Requirement</span></span> | <span data-ttu-id="5c94d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5c94d-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c94d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c94d-129">Header</span></span><br/> | <dl> <span data-ttu-id="5c94d-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c94d-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="5c94d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5c94d-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="5c94d-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c94d-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c94d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c94d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c94d-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="5c94d-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
