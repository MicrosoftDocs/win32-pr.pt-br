---
description: Ajusta o brilho.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: Propriedade MFPKEY_COLOR_BRIGHTNESS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828217"
---
# <a name="mfpkey_color_brightness-property"></a><span data-ttu-id="cdec3-103">Propriedade de brilho de \_ cor do MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="cdec3-103">MFPKEY\_COLOR\_BRIGHTNESS Property</span></span>

<span data-ttu-id="cdec3-104">Ajusta o brilho.</span><span class="sxs-lookup"><span data-stu-id="cdec3-104">Adjusts the brightness.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cdec3-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cdec3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cdec3-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="cdec3-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="cdec3-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="cdec3-107">Data Type</span></span>

<span data-ttu-id="cdec3-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="cdec3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="cdec3-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="cdec3-109">Default Value</span></span>

<span data-ttu-id="cdec3-110">0</span><span class="sxs-lookup"><span data-stu-id="cdec3-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="cdec3-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="cdec3-111">Applies To</span></span>

-   [<span data-ttu-id="cdec3-112">DSP de transformação de controle de cores</span><span class="sxs-lookup"><span data-stu-id="cdec3-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="cdec3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdec3-113">Remarks</span></span>

<span data-ttu-id="cdec3-114">O ajuste de brilho é executado pela adição de um valor ao canal Luma.</span><span class="sxs-lookup"><span data-stu-id="cdec3-114">Brightness adjustment is performed by adding a value to the luma channel.</span></span>

<span data-ttu-id="cdec3-115">Essa propriedade tem um intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="cdec3-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="cdec3-116">Zero indica nenhuma alteração no brilho.</span><span class="sxs-lookup"><span data-stu-id="cdec3-116">Zero indicates no change in brightness.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdec3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdec3-117">Requirements</span></span>



| <span data-ttu-id="cdec3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdec3-118">Requirement</span></span> | <span data-ttu-id="cdec3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cdec3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdec3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdec3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cdec3-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cdec3-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cdec3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdec3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cdec3-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cdec3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cdec3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cdec3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdec3-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdec3-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdec3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdec3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdec3-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cdec3-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
