---
description: Especifica se o codificador usa a codificação de VBR média controlável.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: Propriedade MFPKEY_AVGCONSTRAINED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772919"
---
# <a name="mfpkey_avgconstrained-property"></a><span data-ttu-id="cb90c-103">\_Propriedade MFPKEY AVGCONSTRAINED</span><span class="sxs-lookup"><span data-stu-id="cb90c-103">MFPKEY\_AVGCONSTRAINED Property</span></span>

<span data-ttu-id="cb90c-104">Especifica se o codificador usa a codificação de VBR média controlável.</span><span class="sxs-lookup"><span data-stu-id="cb90c-104">Specifies whether the encoder uses average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cb90c-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cb90c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cb90c-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="cb90c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="cb90c-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="cb90c-107">Data Type</span></span>

<span data-ttu-id="cb90c-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cb90c-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="cb90c-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="cb90c-109">Default Value</span></span>

<span data-ttu-id="cb90c-110">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="cb90c-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="cb90c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb90c-111">Remarks</span></span>

<span data-ttu-id="cb90c-112">Se essa propriedade e a propriedade [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) forem definidas como **Variant \_ true**, o codificador usará a codificação de VBR média controlável.</span><span class="sxs-lookup"><span data-stu-id="cb90c-112">If this property and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="cb90c-113">Nesse caso, o codificador se configura de acordo com os valores de [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) e [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="cb90c-113">In that case, the encoder configures itself according to the values of [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) and [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb90c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb90c-114">Requirements</span></span>



| <span data-ttu-id="cb90c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb90c-115">Requirement</span></span> | <span data-ttu-id="cb90c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cb90c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb90c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb90c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb90c-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb90c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cb90c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb90c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb90c-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb90c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb90c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb90c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb90c-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb90c-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb90c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb90c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb90c-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb90c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
