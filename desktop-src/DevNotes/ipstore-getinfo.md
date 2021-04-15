---
description: Retorna informações sobre o provedor de armazenamento.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'Método IPStore:: GetInfo (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753683"
---
# <a name="ipstoregetinfo-method"></a><span data-ttu-id="f0712-103">Método IPStore:: GetInfo</span><span class="sxs-lookup"><span data-stu-id="f0712-103">IPStore::GetInfo method</span></span>

<span data-ttu-id="f0712-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0712-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f0712-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f0712-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f0712-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="f0712-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f0712-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f0712-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f0712-108">Retorna informações sobre o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f0712-108">Returns information on the storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0712-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0712-109">Syntax</span></span>


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="f0712-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0712-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0712-111">*ppProperties* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f0712-111">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0712-112">Um ponteiro para uma estrutura **PPST \_ PROVIDERINFO** que contém informações sobre o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f0712-112">A pointer to a **PPST\_PROVIDERINFO** structure that contains information about the storage provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0712-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0712-113">Return value</span></span>

<span data-ttu-id="f0712-114">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0712-114">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="f0712-115">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f0712-115">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0712-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0712-116">Requirements</span></span>



| <span data-ttu-id="f0712-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0712-117">Requirement</span></span> | <span data-ttu-id="f0712-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f0712-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0712-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0712-119">Header</span></span><br/> | <dl> <span data-ttu-id="f0712-120"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0712-120"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="f0712-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f0712-121">DLL</span></span><br/>    | <dl> <span data-ttu-id="f0712-122"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0712-122"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0712-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0712-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0712-124">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="f0712-124">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
