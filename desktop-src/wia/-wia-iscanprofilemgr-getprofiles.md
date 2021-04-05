---
description: Obtém todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Método IScanProfileMgr:: getprofiles (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662203"
---
# <a name="iscanprofilemgrgetprofiles-method"></a><span data-ttu-id="05e0d-103">Método IScanProfileMgr:: getprofiles</span><span class="sxs-lookup"><span data-stu-id="05e0d-103">IScanProfileMgr::GetProfiles method</span></span>

<span data-ttu-id="05e0d-104">Obtém todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="05e0d-104">Gets all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05e0d-105">Syntax</span></span>


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="05e0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05e0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05e0d-107">*pulNumProfiles* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="05e0d-107">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05e0d-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="05e0d-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="05e0d-109">Quando passado, um ponteiro para o número máximo de perfis a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="05e0d-109">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="05e0d-110">Quando retornado, um ponteiro para o número de perfis retornado.</span><span class="sxs-lookup"><span data-stu-id="05e0d-110">When returned, a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="05e0d-111">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="05e0d-111">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05e0d-112">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="05e0d-112">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="05e0d-113">O endereço de uma matriz de ponteiros para perfis.</span><span class="sxs-lookup"><span data-stu-id="05e0d-113">The address of an array of pointers to profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05e0d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05e0d-114">Return value</span></span>

<span data-ttu-id="05e0d-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="05e0d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="05e0d-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="05e0d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05e0d-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05e0d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="05e0d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="05e0d-118">Remarks</span></span>

<span data-ttu-id="05e0d-119">Se o número total de perfis disponíveis para o usuário for menor do que o valor passado para *pulNumProfiles*, então *pulNumProfiles* retornará esse total.</span><span class="sxs-lookup"><span data-stu-id="05e0d-119">If the total number of profiles available for the user is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="05e0d-120">Caso contrário, ele retorna o mesmo valor que foi passado para ele.</span><span class="sxs-lookup"><span data-stu-id="05e0d-120">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e0d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05e0d-121">Requirements</span></span>



| <span data-ttu-id="05e0d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="05e0d-122">Requirement</span></span> | <span data-ttu-id="05e0d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="05e0d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="05e0d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05e0d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="05e0d-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05e0d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="05e0d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05e0d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="05e0d-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05e0d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05e0d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05e0d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="05e0d-129"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="05e0d-129"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="05e0d-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="05e0d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05e0d-131"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05e0d-131"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05e0d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="05e0d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e0d-133">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="05e0d-133">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="05e0d-134">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="05e0d-134">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




