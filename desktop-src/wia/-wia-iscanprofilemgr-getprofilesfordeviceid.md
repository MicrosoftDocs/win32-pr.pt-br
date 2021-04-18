---
description: Obtém todos os perfis de verificação associados a um dispositivo.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'Método IScanProfileMgr:: GetProfilesforDeviceID (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789348"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a><span data-ttu-id="6c8bc-103">Método IScanProfileMgr:: GetProfilesforDeviceID</span><span class="sxs-lookup"><span data-stu-id="6c8bc-103">IScanProfileMgr::GetProfilesforDeviceID method</span></span>

<span data-ttu-id="6c8bc-104">Obtém todos os perfis de verificação associados a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-104">Gets all the scan profiles associated with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c8bc-105">Syntax</span></span>


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="6c8bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c8bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8bc-107">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c8bc-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8bc-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6c8bc-108">Type: **BSTR**</span></span>

<span data-ttu-id="6c8bc-109">A ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="6c8bc-110">*pulNumProfiles* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6c8bc-110">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8bc-111">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="6c8bc-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="6c8bc-112">Quando passado, um ponteiro para o número máximo de perfis a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-112">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="6c8bc-113">Quando retornado, o ponteiro para o número de perfis retornado.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-113">When returned, the a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="6c8bc-114">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c8bc-114">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8bc-115">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6c8bc-115">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="6c8bc-116">O endereço de um ponteiro para uma matriz de perfis.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-116">The address of a pointer to an array of profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8bc-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c8bc-117">Return value</span></span>

<span data-ttu-id="6c8bc-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c8bc-118">Type: **HRESULT**</span></span>

<span data-ttu-id="6c8bc-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c8bc-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c8bc-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8bc-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c8bc-121">Remarks</span></span>

<span data-ttu-id="6c8bc-122">Se o número total de perfis associados ao dispositivo for menor do que o valor passado para *pulNumProfiles*, então *pulNumProfiles* retornará esse total.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-122">If the total number of profiles associated with the device is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="6c8bc-123">Caso contrário, ele retorna o mesmo valor que foi passado para ele.</span><span class="sxs-lookup"><span data-stu-id="6c8bc-123">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8bc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c8bc-124">Requirements</span></span>



| <span data-ttu-id="6c8bc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c8bc-125">Requirement</span></span> | <span data-ttu-id="6c8bc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6c8bc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8bc-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c8bc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8bc-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c8bc-128">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6c8bc-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c8bc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8bc-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c8bc-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c8bc-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c8bc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c8bc-132"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8bc-132"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="6c8bc-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="6c8bc-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c8bc-134"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c8bc-134"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8bc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c8bc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8bc-136">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="6c8bc-136">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="6c8bc-137">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="6c8bc-137">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




