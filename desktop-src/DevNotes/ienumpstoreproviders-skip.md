---
description: 'Método IEnumPStoreProviders:: Skip – ignora o próximo número especificado de itens na sequência de enumeração.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: 'Método IEnumPStoreProviders:: Skip (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096744"
---
# <a name="ienumpstoreprovidersskip-method"></a><span data-ttu-id="f2eaa-103">Método IEnumPStoreProviders:: Skip</span><span class="sxs-lookup"><span data-stu-id="f2eaa-103">IEnumPStoreProviders::Skip method</span></span>

<span data-ttu-id="f2eaa-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f2eaa-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f2eaa-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f2eaa-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f2eaa-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f2eaa-108">Ignora o próximo número especificado de itens na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2eaa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2eaa-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="f2eaa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2eaa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2eaa-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2eaa-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eaa-112">O número de tipos de provedor a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="f2eaa-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2eaa-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f2eaa-113">Return value</span></span>

<span data-ttu-id="f2eaa-114">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2eaa-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2eaa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2eaa-115">Requirements</span></span>



| <span data-ttu-id="f2eaa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2eaa-116">Requirement</span></span> | <span data-ttu-id="f2eaa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f2eaa-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2eaa-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2eaa-118">Header</span></span><br/> | <dl> <span data-ttu-id="f2eaa-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2eaa-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="f2eaa-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f2eaa-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="f2eaa-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2eaa-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2eaa-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f2eaa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2eaa-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="f2eaa-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
