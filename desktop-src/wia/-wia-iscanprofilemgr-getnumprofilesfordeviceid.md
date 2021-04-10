---
description: Obtém o número de perfis de verificação para o dispositivo.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Método IScanProfileMgr:: GetNumProfilesforDeviceID (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164707"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a><span data-ttu-id="103b5-103">Método IScanProfileMgr:: GetNumProfilesforDeviceID</span><span class="sxs-lookup"><span data-stu-id="103b5-103">IScanProfileMgr::GetNumProfilesforDeviceID method</span></span>

<span data-ttu-id="103b5-104">Obtém o número de perfis de verificação para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="103b5-104">Gets the number of scan profiles for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="103b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="103b5-105">Syntax</span></span>


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="103b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="103b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="103b5-107">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="103b5-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="103b5-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="103b5-108">Type: **BSTR**</span></span>

<span data-ttu-id="103b5-109">A ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="103b5-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="103b5-110">*pulNumProfiles* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="103b5-110">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="103b5-111">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="103b5-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="103b5-112">Um ponteiro para o número de perfis disponíveis para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="103b5-112">A pointer to the number of profiles available for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="103b5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="103b5-113">Return value</span></span>

<span data-ttu-id="103b5-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="103b5-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="103b5-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="103b5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="103b5-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="103b5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="103b5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="103b5-117">Requirements</span></span>



| <span data-ttu-id="103b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="103b5-118">Requirement</span></span> | <span data-ttu-id="103b5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="103b5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="103b5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="103b5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="103b5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="103b5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="103b5-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="103b5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="103b5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="103b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="103b5-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="103b5-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="103b5-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="103b5-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="103b5-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="103b5-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103b5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="103b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103b5-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="103b5-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="103b5-130">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="103b5-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




