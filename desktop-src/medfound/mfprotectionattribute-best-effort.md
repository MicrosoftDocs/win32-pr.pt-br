---
description: Defina como um atributo para um objeto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Atributo MFPROTECTIONATTRIBUTE_BEST_EFFORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165296"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a><span data-ttu-id="89537-103">\_Atributo de melhor esforço do MFPROTECTIONATTRIBUTE \_</span><span class="sxs-lookup"><span data-stu-id="89537-103">MFPROTECTIONATTRIBUTE\_BEST\_EFFORT attribute</span></span>

<span data-ttu-id="89537-104">Defina como um atributo para um objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="89537-104">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span> <span data-ttu-id="89537-105">Se esse atributo estiver presente, uma tentativa com falha de aplicar a proteção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="89537-105">If this attribute is present, a failed attempt to apply the protection is ignored.</span></span> <span data-ttu-id="89537-106">Se o valor do atributo associado for **true**, o esquema de proteção com o atributo de [ \_ failover \_ MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) deverá ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="89537-106">If the associated attribute value is **TRUE**, the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute should be applied.</span></span>

## <a name="data-type"></a><span data-ttu-id="89537-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="89537-107">Data type</span></span>

<span data-ttu-id="89537-108">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="89537-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="89537-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="89537-109">Remarks</span></span>

<span data-ttu-id="89537-110">Se **verdadeiro**, aplique o esquema de proteção com o atributo de [ \_ \_ failover MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) se a configuração dessa proteção falhar.</span><span class="sxs-lookup"><span data-stu-id="89537-110">If **TRUE**, enforce the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute if setting this protection fails.</span></span>

<span data-ttu-id="89537-111">Defina como um atributo para um objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="89537-111">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="89537-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89537-112">Requirements</span></span>



| <span data-ttu-id="89537-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="89537-113">Requirement</span></span> | <span data-ttu-id="89537-114">Valor</span><span class="sxs-lookup"><span data-stu-id="89537-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89537-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89537-115">Minimum supported client</span></span><br/> | <span data-ttu-id="89537-116">\[Somente aplicativos UWP do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="89537-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="89537-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89537-117">Minimum supported server</span></span><br/> | <span data-ttu-id="89537-118">Somente aplicativos UWP do Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="89537-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="89537-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89537-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="89537-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89537-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89537-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="89537-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89537-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89537-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="89537-123">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="89537-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




