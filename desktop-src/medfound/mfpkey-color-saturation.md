---
description: Ajusta a saturação.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Propriedade MFPKEY_COLOR_SATURATION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505738"
---
# <a name="mfpkey_color_saturation-property"></a><span data-ttu-id="448bc-103">Propriedade de saturação de \_ cor MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="448bc-103">MFPKEY\_COLOR\_SATURATION Property</span></span>

<span data-ttu-id="448bc-104">Ajusta a saturação.</span><span class="sxs-lookup"><span data-stu-id="448bc-104">Adjusts the saturation.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="448bc-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="448bc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="448bc-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="448bc-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="448bc-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="448bc-107">Data Type</span></span>

<span data-ttu-id="448bc-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="448bc-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="448bc-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="448bc-109">Default Value</span></span>

<span data-ttu-id="448bc-110">0</span><span class="sxs-lookup"><span data-stu-id="448bc-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="448bc-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="448bc-111">Applies To</span></span>

-   [<span data-ttu-id="448bc-112">DSP de transformação de controle de cores</span><span class="sxs-lookup"><span data-stu-id="448bc-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="448bc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="448bc-113">Remarks</span></span>

<span data-ttu-id="448bc-114">O ajuste de saturação é executado multiplicando os valores CB e CR por uma constante.</span><span class="sxs-lookup"><span data-stu-id="448bc-114">Saturation adjustment is performed by multiplying the Cb and Cr values by a constant.</span></span>

<span data-ttu-id="448bc-115">Essa propriedade tem um intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="448bc-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="448bc-116">Zero indica nenhuma alteração na saturação.</span><span class="sxs-lookup"><span data-stu-id="448bc-116">Zero indicates no change in saturation.</span></span>

## <a name="requirements"></a><span data-ttu-id="448bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="448bc-117">Requirements</span></span>



| <span data-ttu-id="448bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="448bc-118">Requirement</span></span> | <span data-ttu-id="448bc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="448bc-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="448bc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="448bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="448bc-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="448bc-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="448bc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="448bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="448bc-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="448bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="448bc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="448bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="448bc-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="448bc-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="448bc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="448bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448bc-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="448bc-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
