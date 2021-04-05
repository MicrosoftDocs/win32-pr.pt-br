---
description: Exclui o perfil de exame especificado.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: 'IScanProfileMgr: método eleteProfile de:D (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921803"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a><span data-ttu-id="4c38e-103">IScanProfileMgr: método eleteProfile de:D</span><span class="sxs-lookup"><span data-stu-id="4c38e-103">IScanProfileMgr::DeleteProfile method</span></span>

<span data-ttu-id="4c38e-104">Exclui o perfil de exame especificado.</span><span class="sxs-lookup"><span data-stu-id="4c38e-104">Deletes the specified scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c38e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c38e-105">Syntax</span></span>


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="4c38e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c38e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c38e-107">*pScanProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c38e-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c38e-108">Tipo: \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="4c38e-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="4c38e-109">Um ponteiro para o perfil.</span><span class="sxs-lookup"><span data-stu-id="4c38e-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c38e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c38e-110">Return value</span></span>

<span data-ttu-id="4c38e-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4c38e-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4c38e-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c38e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c38e-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c38e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c38e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c38e-114">Remarks</span></span>

<span data-ttu-id="4c38e-115">**IScanProfileMgr::D eleteprofile** exclui o perfil do disco e destrói o objeto de perfil na memória.</span><span class="sxs-lookup"><span data-stu-id="4c38e-115">**IScanProfileMgr::DeleteProfile** deletes the profile from disk and destroys the profile object in memory.</span></span>

<span data-ttu-id="4c38e-116">Use o método [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) quando mais de um objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) puderem criar ou excluir perfis ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="4c38e-116">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c38e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c38e-117">Requirements</span></span>



| <span data-ttu-id="4c38e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c38e-118">Requirement</span></span> | <span data-ttu-id="4c38e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4c38e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c38e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c38e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c38e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c38e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4c38e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c38e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c38e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c38e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c38e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c38e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c38e-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c38e-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="4c38e-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="4c38e-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c38e-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c38e-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c38e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c38e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c38e-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="4c38e-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="4c38e-130">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="4c38e-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




