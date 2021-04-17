---
description: Obtém um objeto enumerador que pode ser usado, por sua vez, para enumerar os provedores de armazenamento protegidos que estão atualmente instalados no sistema.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Função PStoreEnumProviders (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748494"
---
# <a name="pstoreenumproviders-function"></a><span data-ttu-id="cd9df-103">Função PStoreEnumProviders</span><span class="sxs-lookup"><span data-stu-id="cd9df-103">PStoreEnumProviders function</span></span>

<span data-ttu-id="cd9df-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd9df-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="cd9df-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="cd9df-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="cd9df-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="cd9df-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="cd9df-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="cd9df-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="cd9df-108">Obtém um objeto enumerador que pode ser usado, por sua vez, para enumerar os provedores de armazenamento protegidos que estão atualmente instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="cd9df-108">Gets an enumerator object that can be used in turn to enumerate the protected storage providers that are currently installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9df-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd9df-109">Syntax</span></span>


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="cd9df-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd9df-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd9df-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cd9df-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="cd9df-112">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cd9df-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd9df-113">*ppenum*</span><span class="sxs-lookup"><span data-stu-id="cd9df-113">*ppenum*</span></span> 
</dt> <dd>

<span data-ttu-id="cd9df-114">Um ponteiro para um ponteiro para uma interface [**IEnumPStoreProviders**](ienumpstoreproviders.md) que pode ser usada para enumerar provedores instalados.</span><span class="sxs-lookup"><span data-stu-id="cd9df-114">A pointer to a pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) interface that can be used to enumerate installed providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd9df-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd9df-115">Return value</span></span>

<span data-ttu-id="cd9df-116">Essa função retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cd9df-116">This function returns an **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd9df-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd9df-117">Remarks</span></span>

<span data-ttu-id="cd9df-118">O componente de armazenamento protegido tem uma arquitetura baseada em provedor.</span><span class="sxs-lookup"><span data-stu-id="cd9df-118">The protected storage component has a provider-based architecture.</span></span> <span data-ttu-id="cd9df-119">Os aplicativos que fazem uso do armazenamento protegido podem especificar quais dos provedores instalados usar ao armazenar e recuperar seus dados.</span><span class="sxs-lookup"><span data-stu-id="cd9df-119">Applications that make use of protected storage can specify which of the installed providers to use when storing and retrieving their data.</span></span>

<span data-ttu-id="cd9df-120">A função **PStoreEnumProviders** é usada para enumerar os provedores de armazenamento protegidos instalados.</span><span class="sxs-lookup"><span data-stu-id="cd9df-120">The **PStoreEnumProviders** function is used to enumerate the installed protected storage providers.</span></span> <span data-ttu-id="cd9df-121">Cada provedor é identificado por um GUID (identificador global exclusivo).</span><span class="sxs-lookup"><span data-stu-id="cd9df-121">Each provider is identified by a globally unique identifier (GUID).</span></span>

<span data-ttu-id="cd9df-122">Até este momento, apenas um provedor de armazenamento protegido já foi escrito.</span><span class="sxs-lookup"><span data-stu-id="cd9df-122">Up to this time, only one protected storage provider has ever been written.</span></span> <span data-ttu-id="cd9df-123">Considerando que o serviço de armazenamento protegido está preterido no momento, é muito improvável que todos os provedores adicionais sejam produzidos.</span><span class="sxs-lookup"><span data-stu-id="cd9df-123">Given that the protected storage service is currently deprecated, it is very unlikely that any additional providers will ever be produced.</span></span> <span data-ttu-id="cd9df-124">Como resultado, essa função não deve ser usada para nenhuma finalidade.</span><span class="sxs-lookup"><span data-stu-id="cd9df-124">As a result, this function should not be used for any purpose.</span></span>

<span data-ttu-id="cd9df-125">Esta função não tem biblioteca de importação associada; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="cd9df-125">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9df-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd9df-126">Requirements</span></span>



| <span data-ttu-id="cd9df-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd9df-127">Requirement</span></span> | <span data-ttu-id="cd9df-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cd9df-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9df-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd9df-129">Header</span></span><br/> | <dl> <span data-ttu-id="cd9df-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9df-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="cd9df-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cd9df-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="cd9df-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd9df-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9df-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd9df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9df-134">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="cd9df-134">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
