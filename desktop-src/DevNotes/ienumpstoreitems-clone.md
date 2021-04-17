---
description: Cria outro enumerador que contém o mesmo estado de enumeração do atual.
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'Método IEnumPStoreItems:: clone (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755633"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="b2327-103">Método IEnumPStoreItems:: clone</span><span class="sxs-lookup"><span data-stu-id="b2327-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="b2327-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2327-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b2327-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b2327-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b2327-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="b2327-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b2327-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b2327-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b2327-108">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="b2327-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2327-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2327-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="b2327-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2327-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2327-111">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b2327-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2327-112">Um ponteiro para um ponteiro [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="b2327-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2327-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2327-113">Return value</span></span>

<span data-ttu-id="b2327-114">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2327-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2327-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2327-115">Requirements</span></span>



| <span data-ttu-id="b2327-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2327-116">Requirement</span></span> | <span data-ttu-id="b2327-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b2327-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2327-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2327-118">Header</span></span><br/> | <dl> <span data-ttu-id="b2327-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2327-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b2327-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b2327-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="b2327-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2327-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2327-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2327-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2327-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="b2327-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
