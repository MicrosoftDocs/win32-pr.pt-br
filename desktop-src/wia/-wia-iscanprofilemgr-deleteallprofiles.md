---
description: Exclui todos os perfis de verificação associados ao dispositivo especificado.
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: 'IScanProfileMgr: método eleteAllProfiles de:D (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011041"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a><span data-ttu-id="5687f-103">IScanProfileMgr: método eleteAllProfiles de:D</span><span class="sxs-lookup"><span data-stu-id="5687f-103">IScanProfileMgr::DeleteAllProfiles method</span></span>

<span data-ttu-id="5687f-104">Exclui todos os perfis de verificação associados ao dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5687f-104">Deletes all the scan profiles associated with the specified device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5687f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5687f-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="5687f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5687f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5687f-107">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5687f-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5687f-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5687f-108">Type: **BSTR**</span></span>

<span data-ttu-id="5687f-109">A ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5687f-109">The ID of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5687f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5687f-110">Return value</span></span>

<span data-ttu-id="5687f-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5687f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="5687f-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5687f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5687f-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5687f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5687f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5687f-114">Requirements</span></span>



| <span data-ttu-id="5687f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5687f-115">Requirement</span></span> | <span data-ttu-id="5687f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5687f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5687f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5687f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5687f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5687f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5687f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5687f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5687f-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5687f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5687f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5687f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5687f-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="5687f-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="5687f-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="5687f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5687f-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5687f-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5687f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5687f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5687f-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="5687f-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="5687f-127">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="5687f-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




