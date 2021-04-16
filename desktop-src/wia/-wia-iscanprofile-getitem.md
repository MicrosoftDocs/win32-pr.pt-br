---
description: Obtém o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'Método IScanProfile:: GetItem (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747715"
---
# <a name="iscanprofilegetitem-method"></a><span data-ttu-id="f6f22-103">Método IScanProfile:: GetItem</span><span class="sxs-lookup"><span data-stu-id="f6f22-103">IScanProfile::GetItem method</span></span>

<span data-ttu-id="f6f22-104">Obtém o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.</span><span class="sxs-lookup"><span data-stu-id="f6f22-104">Gets the GUID of the category of the Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6f22-105">Syntax</span></span>


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="f6f22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6f22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f22-107">*pguidCategory* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f6f22-107">*pguidCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6f22-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f6f22-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="f6f22-109">Um ponteiro para o GUID da categoria do item WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f6f22-109">A pointer to the GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="f6f22-110">Essa é sempre uma das constantes da \_ categoria de item IPA do WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f6f22-110">This is always one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f22-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6f22-111">Return value</span></span>

<span data-ttu-id="f6f22-112">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f6f22-112">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f6f22-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f6f22-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6f22-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6f22-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f22-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6f22-115">Requirements</span></span>



| <span data-ttu-id="f6f22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6f22-116">Requirement</span></span> | <span data-ttu-id="f6f22-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f6f22-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f22-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6f22-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f22-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6f22-119">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f6f22-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6f22-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f22-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6f22-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6f22-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6f22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f22-123"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f22-123"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="f6f22-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="f6f22-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6f22-125"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6f22-125"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f22-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6f22-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f22-127">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="f6f22-127">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="f6f22-128">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="f6f22-128">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




