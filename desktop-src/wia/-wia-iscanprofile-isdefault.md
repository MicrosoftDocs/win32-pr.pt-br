---
description: Obtém um valor que indica se o perfil é o perfil de exame padrão de um dispositivo IWiaItem2 associado.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Método IScanProfile:: IsDefault (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921070"
---
# <a name="iscanprofileisdefault-method"></a><span data-ttu-id="62066-103">Método IScanProfile:: IsDefault</span><span class="sxs-lookup"><span data-stu-id="62066-103">IScanProfile::IsDefault method</span></span>

<span data-ttu-id="62066-104">Obtém um valor que indica se o perfil é o perfil de exame padrão de um dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associado.</span><span class="sxs-lookup"><span data-stu-id="62066-104">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="62066-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62066-105">Syntax</span></span>


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a><span data-ttu-id="62066-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62066-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62066-107">*pbDefault* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="62066-107">*pbDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62066-108">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="62066-108">Type: \**BOOL\** _</span></span>

<span data-ttu-id="62066-109">Um ponteiro para um _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="62066-109">A pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="62066-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span><span class="sxs-lookup"><span data-stu-id="62066-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="62066-111">O perfil é o padrão.</span><span class="sxs-lookup"><span data-stu-id="62066-111">The profile is the default.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="62066-112"><span id="FALSE"></span><span id="false"></span>**FOR**</span><span class="sxs-lookup"><span data-stu-id="62066-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="62066-113">O perfil não é o padrão.</span><span class="sxs-lookup"><span data-stu-id="62066-113">The profile is not the default.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62066-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62066-114">Return value</span></span>

<span data-ttu-id="62066-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="62066-115">Type: **HRESULT**</span></span>

<span data-ttu-id="62066-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62066-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62066-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62066-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62066-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="62066-118">Remarks</span></span>

<span data-ttu-id="62066-119">*pbDefault* será **true** se o perfil contiver um `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="62066-119">*pbDefault* is **TRUE** if the profile contains a `<Default>` element.</span></span> <span data-ttu-id="62066-120">Será **false** se nenhum elemento desse tipo estiver presente.</span><span class="sxs-lookup"><span data-stu-id="62066-120">It is **FALSE** if no such element is present.</span></span> <span data-ttu-id="62066-121">O elemento não tem valor.</span><span class="sxs-lookup"><span data-stu-id="62066-121">The element has no value.</span></span>

## <a name="requirements"></a><span data-ttu-id="62066-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62066-122">Requirements</span></span>



| <span data-ttu-id="62066-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="62066-123">Requirement</span></span> | <span data-ttu-id="62066-124">Valor</span><span class="sxs-lookup"><span data-stu-id="62066-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="62066-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62066-125">Minimum supported client</span></span><br/> | <span data-ttu-id="62066-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62066-126">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="62066-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62066-127">Minimum supported server</span></span><br/> | <span data-ttu-id="62066-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62066-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62066-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62066-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="62066-130"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="62066-130"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="62066-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="62066-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62066-132"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62066-132"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62066-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="62066-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62066-134">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="62066-134">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="62066-135">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="62066-135">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




