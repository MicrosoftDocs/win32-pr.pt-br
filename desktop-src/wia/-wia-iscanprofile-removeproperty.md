---
description: Remove uma lista especificada de propriedades filho no <Properties> elemento de um perfil de verificação.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Método IScanProfile:: RemoveProperty (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090809"
---
# <a name="iscanprofileremoveproperty-method"></a><span data-ttu-id="de9fe-104">Método IScanProfile:: RemoveProperty</span><span class="sxs-lookup"><span data-stu-id="de9fe-104">IScanProfile::RemoveProperty method</span></span>

<span data-ttu-id="de9fe-105">Remove uma lista especificada de propriedades filho no `<Properties>` elemento de um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="de9fe-105">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9fe-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de9fe-106">Syntax</span></span>


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a><span data-ttu-id="de9fe-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de9fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de9fe-108">*número* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="de9fe-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de9fe-109">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="de9fe-109">Type: **ULONG**</span></span>

<span data-ttu-id="de9fe-110">O número de entradas na matriz para as quais a *pid* aponta.</span><span class="sxs-lookup"><span data-stu-id="de9fe-110">The number of entries in the array that *pid* points to.</span></span>

</dd> <dt>

<span data-ttu-id="de9fe-111">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de9fe-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de9fe-112">Tipo: \**Propid \** _</span><span class="sxs-lookup"><span data-stu-id="de9fe-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="de9fe-113">Um ponteiro para uma matriz de números de identificação das propriedades a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="de9fe-113">A pointer to an array of identification numbers of the properties to be deleted.</span></span> <span data-ttu-id="de9fe-114">Cada uma é uma [constante de propriedade WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="de9fe-114">Each is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de9fe-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de9fe-115">Return value</span></span>

<span data-ttu-id="de9fe-116">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="de9fe-116">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="de9fe-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="de9fe-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de9fe-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de9fe-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de9fe-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="de9fe-119">Remarks</span></span>

<span data-ttu-id="de9fe-120">Cada valor na matriz que *pid* aponta para é uma das constantes da [Propriedade WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="de9fe-120">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="de9fe-121">Você pode estender esse sistema de identificação.</span><span class="sxs-lookup"><span data-stu-id="de9fe-121">You can extend this identification system.</span></span> <span data-ttu-id="de9fe-122">Consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="de9fe-122">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="de9fe-123">As alterações em um perfil não são salvas no disco até que o aplicativo chame o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="de9fe-123">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="de9fe-124">Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo gravar alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last serão salvas no disco.</span><span class="sxs-lookup"><span data-stu-id="de9fe-124">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9fe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de9fe-125">Requirements</span></span>



| <span data-ttu-id="de9fe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9fe-126">Requirement</span></span> | <span data-ttu-id="de9fe-127">Valor</span><span class="sxs-lookup"><span data-stu-id="de9fe-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="de9fe-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de9fe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="de9fe-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de9fe-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="de9fe-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de9fe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="de9fe-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de9fe-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de9fe-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de9fe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="de9fe-133"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="de9fe-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="de9fe-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="de9fe-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de9fe-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de9fe-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9fe-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="de9fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9fe-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="de9fe-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="de9fe-138">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="de9fe-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de9fe-139">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="de9fe-139">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="de9fe-140">Constantes da propriedade WIA</span><span class="sxs-lookup"><span data-stu-id="de9fe-140">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="de9fe-141">Definindo propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="de9fe-141">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




