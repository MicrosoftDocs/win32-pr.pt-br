---
description: Retorna o GUID do perfil.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'Método IScanProfile:: GetGuid (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296451"
---
# <a name="iscanprofilegetguid-method"></a><span data-ttu-id="d0fbe-103">Método IScanProfile:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="d0fbe-103">IScanProfile::GetGUID method</span></span>

<span data-ttu-id="d0fbe-104">Retorna o GUID do perfil.</span><span class="sxs-lookup"><span data-stu-id="d0fbe-104">Returns the GUID of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0fbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0fbe-105">Syntax</span></span>


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a><span data-ttu-id="d0fbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0fbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0fbe-107">*retval* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d0fbe-107">*retVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0fbe-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="d0fbe-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="d0fbe-109">Um ponteiro para o GUID do perfil.</span><span class="sxs-lookup"><span data-stu-id="d0fbe-109">A pointer to the GUID of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0fbe-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0fbe-110">Return value</span></span>

<span data-ttu-id="d0fbe-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d0fbe-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d0fbe-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d0fbe-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0fbe-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0fbe-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0fbe-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0fbe-114">Remarks</span></span>

<span data-ttu-id="d0fbe-115">O GUID de um perfil é gerado automaticamente quando o perfil é criado com [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span><span class="sxs-lookup"><span data-stu-id="d0fbe-115">The GUID for a profile is automatically generated when the profile is created with [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0fbe-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0fbe-116">Requirements</span></span>



| <span data-ttu-id="d0fbe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0fbe-117">Requirement</span></span> | <span data-ttu-id="d0fbe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d0fbe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fbe-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0fbe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0fbe-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0fbe-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d0fbe-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0fbe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0fbe-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0fbe-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0fbe-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0fbe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0fbe-124"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0fbe-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="d0fbe-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="d0fbe-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0fbe-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0fbe-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0fbe-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0fbe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fbe-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="d0fbe-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="d0fbe-129">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="d0fbe-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




