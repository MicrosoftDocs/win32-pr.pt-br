---
description: Define o valor das propriedades filho especificadas no <Properties> elemento de um perfil de verificação.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Método IScanProfile:: SetProperty (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647488"
---
# <a name="iscanprofilesetproperty-method"></a><span data-ttu-id="71a20-104">Método IScanProfile:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="71a20-104">IScanProfile::SetProperty method</span></span>

<span data-ttu-id="71a20-105">Define o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="71a20-105">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a20-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71a20-106">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="71a20-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71a20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71a20-108">*número* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="71a20-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a20-109">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="71a20-109">Type: **ULONG**</span></span>

<span data-ttu-id="71a20-110">O número de entradas nas matrizes que são apontadas por *pid* e *pvar*.</span><span class="sxs-lookup"><span data-stu-id="71a20-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="71a20-111">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71a20-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a20-112">Tipo: \**Propid \** _</span><span class="sxs-lookup"><span data-stu-id="71a20-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="71a20-113">Um ponteiro para uma matriz de números de identificação das propriedades a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="71a20-113">A pointer to an array of identification numbers of the properties to be set.</span></span> <span data-ttu-id="71a20-114">Cada valor na matriz é uma [constante de propriedade WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="71a20-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="71a20-115">_pvar \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71a20-115">_pvar\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a20-116">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="71a20-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="71a20-117">Um ponteiro para uma matriz de valores a serem atribuídos às propriedades.</span><span class="sxs-lookup"><span data-stu-id="71a20-117">A pointer to an array of values to be assigned to the properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71a20-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71a20-118">Return value</span></span>

<span data-ttu-id="71a20-119">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="71a20-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="71a20-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="71a20-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71a20-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71a20-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71a20-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="71a20-122">Remarks</span></span>

<span data-ttu-id="71a20-123">Cada valor na matriz que *pid* aponta para é uma das constantes da [Propriedade WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="71a20-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="71a20-124">Você pode estender esse sistema de identificação.</span><span class="sxs-lookup"><span data-stu-id="71a20-124">You can extend this identification system.</span></span> <span data-ttu-id="71a20-125">Consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="71a20-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="71a20-126">As alterações em um perfil não são salvas no disco até que o aplicativo chame o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="71a20-126">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="71a20-127">Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo gravar alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last serão salvas no disco.</span><span class="sxs-lookup"><span data-stu-id="71a20-127">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="71a20-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71a20-128">Requirements</span></span>



| <span data-ttu-id="71a20-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a20-129">Requirement</span></span> | <span data-ttu-id="71a20-130">Valor</span><span class="sxs-lookup"><span data-stu-id="71a20-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a20-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a20-131">Minimum supported client</span></span><br/> | <span data-ttu-id="71a20-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71a20-132">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="71a20-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a20-133">Minimum supported server</span></span><br/> | <span data-ttu-id="71a20-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71a20-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71a20-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71a20-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="71a20-136"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="71a20-136"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="71a20-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="71a20-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71a20-138"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71a20-138"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a20-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="71a20-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a20-140">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="71a20-140">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="71a20-141">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="71a20-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71a20-142">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="71a20-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="71a20-143">Constantes da propriedade WIA</span><span class="sxs-lookup"><span data-stu-id="71a20-143">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="71a20-144">Definindo propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="71a20-144">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
