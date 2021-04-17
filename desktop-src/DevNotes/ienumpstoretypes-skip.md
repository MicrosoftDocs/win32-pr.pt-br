---
description: Ignora o próximo número especificado de itens na sequência de enumeração.
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'Método IEnumPStoreTypes:: Skip (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 511595dd55f66e91ae0f5606f9e047918e7ff0fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752572"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="123ec-103">Método IEnumPStoreTypes:: Skip</span><span class="sxs-lookup"><span data-stu-id="123ec-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="123ec-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="123ec-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="123ec-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="123ec-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="123ec-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="123ec-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="123ec-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="123ec-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="123ec-108">Ignora o próximo número especificado de itens na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="123ec-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="123ec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="123ec-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="123ec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="123ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="123ec-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="123ec-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="123ec-112">O número de tipos de provedor a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="123ec-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="123ec-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="123ec-113">Return value</span></span>

<span data-ttu-id="123ec-114">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="123ec-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="123ec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="123ec-115">Requirements</span></span>



| <span data-ttu-id="123ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="123ec-116">Requirement</span></span> | <span data-ttu-id="123ec-117">Valor</span><span class="sxs-lookup"><span data-stu-id="123ec-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="123ec-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="123ec-118">Header</span></span><br/> | <dl> <span data-ttu-id="123ec-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="123ec-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="123ec-120">DLL</span><span class="sxs-lookup"><span data-stu-id="123ec-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="123ec-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123ec-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="123ec-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="123ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123ec-123">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="123ec-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
