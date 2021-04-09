---
description: Obtém o número de IDs de propriedade em um perfil.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'Método IScanProfile:: GetNumPropIDS (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090811"
---
# <a name="iscanprofilegetnumpropids-method"></a><span data-ttu-id="7931f-103">Método IScanProfile:: GetNumPropIDS</span><span class="sxs-lookup"><span data-stu-id="7931f-103">IScanProfile::GetNumPropIDS method</span></span>

<span data-ttu-id="7931f-104">Obtém o número de IDs de propriedade em um perfil.</span><span class="sxs-lookup"><span data-stu-id="7931f-104">Gets the number of property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="7931f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7931f-105">Syntax</span></span>


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a><span data-ttu-id="7931f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7931f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7931f-107">*número* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="7931f-107">*num* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7931f-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="7931f-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="7931f-109">O número de IDs de propriedade no perfil.</span><span class="sxs-lookup"><span data-stu-id="7931f-109">The number of property IDs in the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7931f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7931f-110">Return value</span></span>

<span data-ttu-id="7931f-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7931f-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7931f-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7931f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7931f-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7931f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7931f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7931f-114">Requirements</span></span>



| <span data-ttu-id="7931f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7931f-115">Requirement</span></span> | <span data-ttu-id="7931f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7931f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7931f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7931f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7931f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7931f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7931f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7931f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7931f-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7931f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7931f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7931f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7931f-122"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="7931f-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="7931f-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="7931f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7931f-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7931f-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7931f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7931f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7931f-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="7931f-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="7931f-127">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="7931f-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




