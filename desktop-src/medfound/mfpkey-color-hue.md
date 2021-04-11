---
description: Ajusta o matiz.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Propriedade MFPKEY_COLOR_HUE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091422"
---
# <a name="mfpkey_color_hue-property"></a><span data-ttu-id="67dde-103">\_Propriedade matiz de cor do MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="67dde-103">MFPKEY\_COLOR\_HUE Property</span></span>

<span data-ttu-id="67dde-104">Ajusta o matiz.</span><span class="sxs-lookup"><span data-stu-id="67dde-104">Adjusts the hue.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="67dde-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="67dde-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="67dde-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="67dde-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="67dde-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="67dde-107">Data Type</span></span>

<span data-ttu-id="67dde-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="67dde-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="67dde-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="67dde-109">Default Value</span></span>

<span data-ttu-id="67dde-110">0</span><span class="sxs-lookup"><span data-stu-id="67dde-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="67dde-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="67dde-111">Applies To</span></span>

-   [<span data-ttu-id="67dde-112">DSP de transformação de controle de cores</span><span class="sxs-lookup"><span data-stu-id="67dde-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="67dde-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="67dde-113">Remarks</span></span>

<span data-ttu-id="67dde-114">O ajuste de matiz é realizado pela combinação dos valores CB e CR.</span><span class="sxs-lookup"><span data-stu-id="67dde-114">Hue adjustment is performed by mixing the Cb and Cr values.</span></span> <span data-ttu-id="67dde-115">(Se CB e CR forem plotados em um espaço bidimensional, o ajuste de matiz será realizado girando em volta da origem.)</span><span class="sxs-lookup"><span data-stu-id="67dde-115">(If Cb and Cr are plotted in a 2-dimensional space, hue adjustment is performed by rotating around the origin.)</span></span>

<span data-ttu-id="67dde-116">Essa propriedade tem um intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="67dde-116">This property has a range of -127 to 127.</span></span> <span data-ttu-id="67dde-117">Zero indica nenhuma alteração no matiz.</span><span class="sxs-lookup"><span data-stu-id="67dde-117">Zero indicates no change in hue.</span></span>

## <a name="requirements"></a><span data-ttu-id="67dde-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67dde-118">Requirements</span></span>



| <span data-ttu-id="67dde-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="67dde-119">Requirement</span></span> | <span data-ttu-id="67dde-120">Valor</span><span class="sxs-lookup"><span data-stu-id="67dde-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67dde-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67dde-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67dde-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="67dde-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="67dde-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67dde-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67dde-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="67dde-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67dde-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67dde-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="67dde-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="67dde-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67dde-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="67dde-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67dde-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67dde-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
