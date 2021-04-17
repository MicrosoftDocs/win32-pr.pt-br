---
description: Especifica se o codificador principal usa o &\# 0034; Mais&\# 0034; recurso.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Propriedade MFPKEY_ENHANCED_WMA (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752388"
---
# <a name="mfpkey_enhanced_wma-property"></a><span data-ttu-id="7a002-103">\_Propriedade WMA MFPKEY Enhanced \_</span><span class="sxs-lookup"><span data-stu-id="7a002-103">MFPKEY\_ENHANCED\_WMA Property</span></span>

<span data-ttu-id="7a002-104">Especifica se o codificador principal usa o recurso "Plus".</span><span class="sxs-lookup"><span data-stu-id="7a002-104">Specifies whether the core encoder uses the "Plus" feature.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7a002-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7a002-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7a002-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7a002-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7a002-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="7a002-107">Data Type</span></span>

<span data-ttu-id="7a002-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="7a002-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="7a002-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="7a002-109">Default Value</span></span>

<span data-ttu-id="7a002-110">0</span><span class="sxs-lookup"><span data-stu-id="7a002-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="7a002-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a002-111">Remarks</span></span>

<span data-ttu-id="7a002-112">Essa propriedade está disponível somente para o Windows Media Audio sem perdas.</span><span class="sxs-lookup"><span data-stu-id="7a002-112">This property is available only for Windows Media Audio Lossless.</span></span>

<span data-ttu-id="7a002-113">Se você deixar essa propriedade com seu valor padrão de 0 ou se defini-la como 1, o codificador principal decidirá se a parte "Plus" deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="7a002-113">If you leave this property at its default value of 0, or if you set it to 1, the core encoder decides whether the "Plus" portion should be used.</span></span> <span data-ttu-id="7a002-114">Se você definir essa propriedade como 2, o codificador principal não usará o recurso "Plus".</span><span class="sxs-lookup"><span data-stu-id="7a002-114">If you set this property to 2, the core encoder does not use the "Plus" feature.</span></span>

<span data-ttu-id="7a002-115">Essa propriedade altera os tipos de mídia enumerados, portanto, se você defini-lo, deverá fazê-lo antes de definir o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="7a002-115">This property alters the enumerated media types, so if you set it, you must do so before you set the output type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a002-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a002-116">Requirements</span></span>



| <span data-ttu-id="7a002-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a002-117">Requirement</span></span> | <span data-ttu-id="7a002-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7a002-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a002-119">Cliente</span><span class="sxs-lookup"><span data-stu-id="7a002-119">Client</span></span><br/> | <span data-ttu-id="7a002-120">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a002-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="7a002-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a002-121">Header</span></span><br/> | <dl> <span data-ttu-id="7a002-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a002-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a002-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a002-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a002-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7a002-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
