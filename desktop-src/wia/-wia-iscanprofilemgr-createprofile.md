---
description: Cria um perfil de verificação vazio e o associa a um scanner ou a outro item de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Método IScanProfileMgr:: CreateProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461203"
---
# <a name="iscanprofilemgrcreateprofile-method"></a><span data-ttu-id="b6e89-103">Método IScanProfileMgr:: CreateProfile</span><span class="sxs-lookup"><span data-stu-id="b6e89-103">IScanProfileMgr::CreateProfile method</span></span>

<span data-ttu-id="b6e89-104">Cria um perfil de verificação vazio e o associa a um scanner ou a outro item de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="b6e89-104">Creates an empty scan profile and associates it with a scanner or other Windows Image Acquisition (WIA) 2.0 item.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6e89-105">Syntax</span></span>


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="b6e89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6e89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e89-107">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e89-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b6e89-108">Type: **BSTR**</span></span>

<span data-ttu-id="b6e89-109">A ID do dispositivo ou o item do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b6e89-109">The ID of the device or WIA 2.0 item.</span></span>

</dd> <dt>

<span data-ttu-id="b6e89-110">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e89-111">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b6e89-111">Type: **BSTR**</span></span>

<span data-ttu-id="b6e89-112">O nome amigável do novo perfil.</span><span class="sxs-lookup"><span data-stu-id="b6e89-112">The friendly name of the new profile.</span></span>

</dd> <dt>

<span data-ttu-id="b6e89-113">*guidCategory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-113">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e89-114">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="b6e89-114">Type: **GUID**</span></span>

<span data-ttu-id="b6e89-115">O GUID da categoria do dispositivo ou do item WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b6e89-115">The GUID of the category of the device or WIA 2.0 item.</span></span> <span data-ttu-id="b6e89-116">Deve ser uma das \_ constantes da categoria de item IPA do WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b6e89-116">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> <dt>

<span data-ttu-id="b6e89-117">*ppScanProfile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-117">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e89-118">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b6e89-118">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="b6e89-119">O endereço de um ponteiro para o novo perfil.</span><span class="sxs-lookup"><span data-stu-id="b6e89-119">The address of a pointer to the new profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6e89-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6e89-120">Return value</span></span>

<span data-ttu-id="b6e89-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b6e89-121">Type: **HRESULT**</span></span>

<span data-ttu-id="b6e89-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b6e89-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6e89-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6e89-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6e89-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6e89-124">Remarks</span></span>

<span data-ttu-id="b6e89-125">**IScanProfileMgr:: CreateProfile** associa o dispositivo especificado ao novo perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="b6e89-125">**IScanProfileMgr::CreateProfile** associates the specified device with the new scan profile.</span></span>

<span data-ttu-id="b6e89-126">**IScanProfileMgr:: CreateProfile** gera automaticamente um GUID para o novo perfil.</span><span class="sxs-lookup"><span data-stu-id="b6e89-126">**IScanProfileMgr::CreateProfile** automatically generates a GUID for the new profile.</span></span> <span data-ttu-id="b6e89-127">Obtenha o GUID com [**GetGUID**](-wia-iscanprofile-getguid.md).</span><span class="sxs-lookup"><span data-stu-id="b6e89-127">Get the GUID with [**GetGUID**](-wia-iscanprofile-getguid.md).</span></span>

<span data-ttu-id="b6e89-128">Use o método [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) quando mais de um objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) puderem criar ou excluir perfis ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b6e89-128">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e89-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e89-129">Requirements</span></span>



| <span data-ttu-id="b6e89-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e89-130">Requirement</span></span> | <span data-ttu-id="b6e89-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b6e89-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e89-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6e89-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e89-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-133">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b6e89-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6e89-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e89-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6e89-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6e89-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e89-137"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6e89-137"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="b6e89-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="b6e89-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6e89-139"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6e89-139"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6e89-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6e89-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e89-141">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="b6e89-141">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="b6e89-142">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="b6e89-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




