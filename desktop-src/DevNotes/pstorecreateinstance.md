---
description: Recupera um ponteiro de interface para um provedor de armazenamento.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Função PStoreCreateInstance (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752567"
---
# <a name="pstorecreateinstance-function"></a><span data-ttu-id="c107f-103">Função PStoreCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c107f-103">PStoreCreateInstance function</span></span>

<span data-ttu-id="c107f-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c107f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="c107f-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c107f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="c107f-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="c107f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="c107f-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="c107f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="c107f-108">\[Essa função pode ser alterada ou indisponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="c107f-108">\[This function may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="c107f-109">Use as funções **CryptProtectData** e **CryptUnprotectData** em vez dessa função.\]</span><span class="sxs-lookup"><span data-stu-id="c107f-109">Use the **CryptProtectData** and **CryptUnprotectData** functions instead of this function.\]</span></span>

<span data-ttu-id="c107f-110">Recupera um ponteiro de interface para um provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c107f-110">Retrieves an interface pointer to a storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="c107f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c107f-111">Syntax</span></span>


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c107f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c107f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c107f-113">*ppProvider* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c107f-113">*ppProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c107f-114">Um ponteiro para o ponteiro de interface recuperado para o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c107f-114">A pointer to the retrieved interface pointer for the storage provider.</span></span> <span data-ttu-id="c107f-115">Quando você terminar de usar a interface, decrementará sua contagem de referência chamando seu método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="c107f-115">When you finish using the interface, decrement its reference count by calling its [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="c107f-116">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c107f-116">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c107f-117">*pProviderID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c107f-117">*pProviderID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c107f-118">Um ponteiro para o **GUID** que identifica o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c107f-118">A pointer to the **GUID** that identifies the storage provider.</span></span> <span data-ttu-id="c107f-119">Se esse parâmetro for **nulo**, o provedor de armazenamento base será usado.</span><span class="sxs-lookup"><span data-stu-id="c107f-119">If this parameter is **NULL**, then the base storage provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="c107f-120">*preservado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c107f-120">*pReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c107f-121">Reservado deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c107f-121">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c107f-122">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c107f-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c107f-123">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c107f-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c107f-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c107f-124">Return value</span></span>

<span data-ttu-id="c107f-125">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c107f-125">The return value is an **HRESULT**.</span></span> <span data-ttu-id="c107f-126">Um valor de **S \_ OK** indica que a função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c107f-126">A value of **S\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c107f-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c107f-127">Remarks</span></span>

<span data-ttu-id="c107f-128">Esta função não tem biblioteca de importação associada; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c107f-128">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c107f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c107f-129">Requirements</span></span>



| <span data-ttu-id="c107f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c107f-130">Requirement</span></span> | <span data-ttu-id="c107f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c107f-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c107f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c107f-132">Header</span></span><br/> | <dl> <span data-ttu-id="c107f-133"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="c107f-133"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="c107f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c107f-134">DLL</span></span><br/>    | <dl> <span data-ttu-id="c107f-135"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c107f-135"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c107f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c107f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c107f-137">**CryptProtectData**</span><span class="sxs-lookup"><span data-stu-id="c107f-137">**CryptProtectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[<span data-ttu-id="c107f-138">**CryptUnprotectData**</span><span class="sxs-lookup"><span data-stu-id="c107f-138">**CryptUnprotectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
