---
description: Define as informações do parâmetro especificado.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'Método IPStore:: SetProvParam (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752371"
---
# <a name="ipstoresetprovparam-method"></a><span data-ttu-id="6ea76-103">Método IPStore:: SetProvParam</span><span class="sxs-lookup"><span data-stu-id="6ea76-103">IPStore::SetProvParam method</span></span>

<span data-ttu-id="6ea76-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ea76-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6ea76-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6ea76-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6ea76-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="6ea76-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6ea76-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6ea76-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6ea76-108">Define as informações do parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="6ea76-108">Sets the specified parameter information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea76-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ea76-109">Syntax</span></span>


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6ea76-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ea76-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea76-111">*dwParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ea76-111">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea76-112">Contém **o \_ \_ \_ \_ cache pw de liberação PP de PST** para liberar o cache de senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ea76-112">Contains **PST\_PP\_FLUSH\_PW\_CACHE** to flush the user password cache.</span></span>

</dd> <dt>

<span data-ttu-id="6ea76-113">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ea76-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea76-114">O comprimento da senha no buffer.</span><span class="sxs-lookup"><span data-stu-id="6ea76-114">The length of the password in the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6ea76-115">*pbData*</span><span class="sxs-lookup"><span data-stu-id="6ea76-115">*pbData*</span></span> 
</dt> <dd>

<span data-ttu-id="6ea76-116">Um ponteiro para um buffer que contém a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ea76-116">A pointer to a buffer that contains the user's password.</span></span> <span data-ttu-id="6ea76-117">Isso deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6ea76-117">This must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6ea76-118">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6ea76-118">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="6ea76-119">Reservado: deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6ea76-119">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea76-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ea76-120">Return value</span></span>

<span data-ttu-id="6ea76-121">O valor de retorno é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ea76-121">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="6ea76-122">Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6ea76-122">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea76-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ea76-123">Requirements</span></span>



| <span data-ttu-id="6ea76-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ea76-124">Requirement</span></span> | <span data-ttu-id="6ea76-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6ea76-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea76-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ea76-126">Header</span></span><br/> | <dl> <span data-ttu-id="6ea76-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ea76-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6ea76-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6ea76-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="6ea76-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ea76-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ea76-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ea76-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea76-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="6ea76-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
