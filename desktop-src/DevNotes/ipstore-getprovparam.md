---
description: Destinado a definir as informações do parâmetro especificado.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Método IPStore:: GetProvParam (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747904"
---
# <a name="ipstoregetprovparam-method"></a><span data-ttu-id="a3e83-103">Método IPStore:: GetProvParam</span><span class="sxs-lookup"><span data-stu-id="a3e83-103">IPStore::GetProvParam method</span></span>

<span data-ttu-id="a3e83-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a3e83-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a3e83-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a3e83-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a3e83-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="a3e83-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a3e83-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a3e83-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a3e83-108">\[Este método não está implementado.\]</span><span class="sxs-lookup"><span data-stu-id="a3e83-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="a3e83-109">Destinado a definir as informações do parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="a3e83-109">Intended to set the specified parameter information.</span></span> <span data-ttu-id="a3e83-110">Observe, no entanto, que ele não está implementado e sempre falhará.</span><span class="sxs-lookup"><span data-stu-id="a3e83-110">Note, however, that it is not implemented and will always fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e83-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3e83-111">Syntax</span></span>


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a3e83-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3e83-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e83-113">*dwParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a3e83-113">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e83-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a3e83-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a3e83-115">*pcbData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3e83-115">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e83-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a3e83-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a3e83-117">*ppbData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3e83-117">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e83-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a3e83-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a3e83-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a3e83-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e83-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a3e83-120">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e83-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3e83-121">Return value</span></span>

<span data-ttu-id="a3e83-122">As chamadas para esse método sempre falharão.</span><span class="sxs-lookup"><span data-stu-id="a3e83-122">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e83-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3e83-123">Requirements</span></span>



| <span data-ttu-id="a3e83-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e83-124">Requirement</span></span> | <span data-ttu-id="a3e83-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e83-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e83-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3e83-126">Header</span></span><br/> | <dl> <span data-ttu-id="a3e83-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e83-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a3e83-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e83-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="a3e83-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e83-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e83-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3e83-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e83-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="a3e83-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
