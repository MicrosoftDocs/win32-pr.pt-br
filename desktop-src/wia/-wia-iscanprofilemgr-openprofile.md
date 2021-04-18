---
description: Abre um perfil de verificação que foi salvo no disco como um arquivo XML.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'Método IScanProfileMgr:: OpenProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785201"
---
# <a name="iscanprofilemgropenprofile-method"></a><span data-ttu-id="48fed-103">Método IScanProfileMgr:: OpenProfile</span><span class="sxs-lookup"><span data-stu-id="48fed-103">IScanProfileMgr::OpenProfile method</span></span>

<span data-ttu-id="48fed-104">Abre um perfil de verificação que foi salvo no disco como um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="48fed-104">Opens a scan profile that has been saved to disk as an XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="48fed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48fed-105">Syntax</span></span>


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="48fed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48fed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48fed-107">*GUID* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="48fed-107">*guid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48fed-108">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="48fed-108">Type: **GUID**</span></span>

<span data-ttu-id="48fed-109">O GUID do perfil.</span><span class="sxs-lookup"><span data-stu-id="48fed-109">The GUID of the profile.</span></span>

</dd> <dt>

<span data-ttu-id="48fed-110">*ppScanProfile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="48fed-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48fed-111">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="48fed-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="48fed-112">O endereço de um ponteiro para o perfil.</span><span class="sxs-lookup"><span data-stu-id="48fed-112">The address of a pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48fed-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48fed-113">Return value</span></span>

<span data-ttu-id="48fed-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48fed-114">Type: **HRESULT**</span></span>

<span data-ttu-id="48fed-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="48fed-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48fed-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48fed-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="48fed-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="48fed-117">Remarks</span></span>

<span data-ttu-id="48fed-118">Se um perfil de verificação for salvo usando o método [**salvar**](-wia-iscanprofile-save.md) , ele será armazenado como um arquivo XML em% USERPROFILE% \\ dados de aplicativo \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="48fed-118">If a scan profile is saved using the [**Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="48fed-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48fed-119">Requirements</span></span>



| <span data-ttu-id="48fed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48fed-120">Requirement</span></span> | <span data-ttu-id="48fed-121">Valor</span><span class="sxs-lookup"><span data-stu-id="48fed-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="48fed-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48fed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="48fed-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48fed-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="48fed-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48fed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="48fed-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48fed-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48fed-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48fed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="48fed-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="48fed-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="48fed-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="48fed-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48fed-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48fed-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48fed-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="48fed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fed-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="48fed-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="48fed-132">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="48fed-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




