---
description: Obtém o nome amigável do perfil.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: 'Método IScanProfile:: GetName (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164709"
---
# <a name="iscanprofilegetname-method"></a><span data-ttu-id="2247d-103">Método IScanProfile:: GetName</span><span class="sxs-lookup"><span data-stu-id="2247d-103">IScanProfile::GetName method</span></span>

<span data-ttu-id="2247d-104">Obtém o nome amigável do perfil.</span><span class="sxs-lookup"><span data-stu-id="2247d-104">Gets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="2247d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2247d-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="2247d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2247d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2247d-107">*pbstrName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2247d-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2247d-108">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="2247d-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="2247d-109">O nome amigável do perfil.</span><span class="sxs-lookup"><span data-stu-id="2247d-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2247d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2247d-110">Return value</span></span>

<span data-ttu-id="2247d-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2247d-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2247d-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2247d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2247d-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2247d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2247d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2247d-114">Remarks</span></span>

<span data-ttu-id="2247d-115">Esse método é necessário porque o GUID de um perfil não pode ser usado para exibir o perfil de verificação para um usuário.</span><span class="sxs-lookup"><span data-stu-id="2247d-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

## <a name="requirements"></a><span data-ttu-id="2247d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2247d-116">Requirements</span></span>



| <span data-ttu-id="2247d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2247d-117">Requirement</span></span> | <span data-ttu-id="2247d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2247d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2247d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2247d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2247d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2247d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2247d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2247d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2247d-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2247d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2247d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2247d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2247d-124"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="2247d-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="2247d-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="2247d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2247d-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2247d-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2247d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2247d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2247d-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="2247d-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="2247d-129">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="2247d-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




