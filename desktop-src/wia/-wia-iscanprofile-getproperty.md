---
description: Obtém o valor das propriedades filho especificadas no <Properties> elemento de um perfil de verificação.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'Método IScanProfile:: GetProperty (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762187"
---
# <a name="iscanprofilegetproperty-method"></a><span data-ttu-id="4005e-104">Método IScanProfile:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="4005e-104">IScanProfile::GetProperty method</span></span>

<span data-ttu-id="4005e-105">Obtém o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="4005e-105">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="4005e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4005e-106">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="4005e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4005e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4005e-108">*número* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="4005e-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4005e-109">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="4005e-109">Type: **ULONG**</span></span>

<span data-ttu-id="4005e-110">O número de entradas nas matrizes que são apontadas por *pid* e *pvar*.</span><span class="sxs-lookup"><span data-stu-id="4005e-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="4005e-111">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4005e-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4005e-112">Tipo: \**Propid \** _</span><span class="sxs-lookup"><span data-stu-id="4005e-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="4005e-113">Um ponteiro para uma matriz dos números de identificação das propriedades a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="4005e-113">A pointer to an array of the identification numbers of the properties to be set.</span></span> <span data-ttu-id="4005e-114">Cada valor na matriz é uma [constante de propriedade WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4005e-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4005e-115">_pvar \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4005e-115">_pvar\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4005e-116">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="4005e-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="4005e-117">Um ponteiro para uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="4005e-117">A pointer to an array of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4005e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4005e-118">Return value</span></span>

<span data-ttu-id="4005e-119">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4005e-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4005e-120">Retornará S \_ false se qualquer um dos valores de propriedade não estiver disponível; caso contrário, retornará S \_ OK ou um código de erro com padrão.</span><span class="sxs-lookup"><span data-stu-id="4005e-120">Returns S\_FALSE if any of the property values is not available; otherwise, returns S\_OK or a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4005e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4005e-121">Remarks</span></span>

<span data-ttu-id="4005e-122">O tipo de cada valor deve ser do mesmo tipo que foi definido com a chamada para [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4005e-122">The type of each value must be the same type that was set with the call to [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).</span></span>

<span data-ttu-id="4005e-123">Cada valor na matriz que *pid* aponta para é uma das constantes da [Propriedade WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4005e-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="4005e-124">Você pode estender esse sistema de identificação.</span><span class="sxs-lookup"><span data-stu-id="4005e-124">You can extend this identification system.</span></span> <span data-ttu-id="4005e-125">Consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4005e-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4005e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4005e-126">Requirements</span></span>



| <span data-ttu-id="4005e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4005e-127">Requirement</span></span> | <span data-ttu-id="4005e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4005e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4005e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4005e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4005e-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4005e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4005e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4005e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4005e-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4005e-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4005e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4005e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4005e-134"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4005e-134"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="4005e-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="4005e-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4005e-136"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4005e-136"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4005e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4005e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4005e-138">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="4005e-138">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="4005e-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4005e-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4005e-140">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="4005e-140">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="4005e-141">Constantes da propriedade WIA</span><span class="sxs-lookup"><span data-stu-id="4005e-141">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="4005e-142">Definindo propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="4005e-142">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
