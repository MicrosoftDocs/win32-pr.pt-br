---
description: Ajusta o contraste.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: Propriedade MFPKEY_COLOR_CONTRAST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785169"
---
# <a name="mfpkey_color_contrast-property"></a><span data-ttu-id="c2426-103">\_Propriedade contraste de cor do MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="c2426-103">MFPKEY\_COLOR\_CONTRAST Property</span></span>

<span data-ttu-id="c2426-104">Ajusta o contraste.</span><span class="sxs-lookup"><span data-stu-id="c2426-104">Adjusts the contrast.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c2426-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c2426-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c2426-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c2426-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c2426-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="c2426-107">Data Type</span></span>

<span data-ttu-id="c2426-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="c2426-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c2426-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="c2426-109">Default Value</span></span>

<span data-ttu-id="c2426-110">0</span><span class="sxs-lookup"><span data-stu-id="c2426-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="c2426-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="c2426-111">Applies To</span></span>

-   [<span data-ttu-id="c2426-112">DSP de transformação de controle de cores</span><span class="sxs-lookup"><span data-stu-id="c2426-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="c2426-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2426-113">Remarks</span></span>

<span data-ttu-id="c2426-114">O ajuste de contraste é executado multiplicando os valores de YCbCr por um fator de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="c2426-114">Contrast adjustment is performed by multiplying the YCbCr values by a scaling factor.</span></span>

<span data-ttu-id="c2426-115">Essa propriedade tem um intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="c2426-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="c2426-116">Zero indica que não há alteração em contraste.</span><span class="sxs-lookup"><span data-stu-id="c2426-116">Zero indicates no change in contrast.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2426-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2426-117">Requirements</span></span>



| <span data-ttu-id="c2426-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2426-118">Requirement</span></span> | <span data-ttu-id="c2426-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c2426-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2426-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2426-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2426-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c2426-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c2426-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2426-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2426-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2426-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2426-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2426-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2426-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2426-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2426-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2426-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2426-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c2426-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
