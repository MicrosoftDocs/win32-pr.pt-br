---
description: Especifica o tamanho da fatia em unidades de megabytes (MB), bits ou MB de linha.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Propriedade CODECAPI_AVEncSliceControlSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089785"
---
# <a name="codecapi_avencslicecontrolsize-property"></a><span data-ttu-id="410d3-103">\_Propriedade CODECAPI AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="410d3-103">CODECAPI\_AVEncSliceControlSize property</span></span>

<span data-ttu-id="410d3-104">Especifica o tamanho da fatia em unidades de megabytes (MB), bits ou MB de linha.</span><span class="sxs-lookup"><span data-stu-id="410d3-104">Specifies the size of the slice in units of megabyte (MB), bits, or MB row.</span></span>

## <a name="data-type"></a><span data-ttu-id="410d3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="410d3-105">Data type</span></span>

<span data-ttu-id="410d3-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="410d3-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="410d3-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="410d3-107">Property GUID</span></span>

<span data-ttu-id="410d3-108">**CODECAPI \_ AVEncSliceControlSize**</span><span class="sxs-lookup"><span data-stu-id="410d3-108">**CODECAPI\_AVEncSliceControlSize**</span></span>

## <a name="remarks"></a><span data-ttu-id="410d3-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="410d3-109">Remarks</span></span>

<span data-ttu-id="410d3-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="410d3-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="410d3-111">O significado do valor de CODECAPI \_ AVEncSliceControlSize é controlado pela propriedade [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) .</span><span class="sxs-lookup"><span data-stu-id="410d3-111">The meaning of the value of CODECAPI\_AVEncSliceControlSize is controlled by the [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) property.</span></span> <span data-ttu-id="410d3-112">A tabela a seguir ilustra como as \_ Propriedades CODECAPI AVEncSliceControlSize e CODECAPI \_ AVEncSliceControlMode controlam o tamanho e o número de fatias em um quadro.</span><span class="sxs-lookup"><span data-stu-id="410d3-112">The following table illustrates how the CODECAPI\_AVEncSliceControlSize and CODECAPI\_AVEncSliceControlMode properties control the size and number of slices in a frame.</span></span>



| <span data-ttu-id="410d3-113">Configuração de CODECAPI \_ AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="410d3-113">CODECAPI\_AVEncSliceControlMode setting</span></span> | <span data-ttu-id="410d3-114">Significado do valor</span><span class="sxs-lookup"><span data-stu-id="410d3-114">Meaning of value</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410d3-115">0</span><span class="sxs-lookup"><span data-stu-id="410d3-115">0</span></span>                                       | <span data-ttu-id="410d3-116">Este é um inteiro que indica o tamanho de cada fatia no quadro em unidades de macroblocos.</span><span class="sxs-lookup"><span data-stu-id="410d3-116">This is an integer that indicates the size of each slice in the frame in units of macroblocks.</span></span> <br/> <span data-ttu-id="410d3-117">O codificador deve rejeitar a configuração quando o valor for maior que o número de macroblocos no quadro.</span><span class="sxs-lookup"><span data-stu-id="410d3-117">The encoder should reject the setting when the value is greater than the number of macroblocks in the frame.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="410d3-118">1</span><span class="sxs-lookup"><span data-stu-id="410d3-118">1</span></span>                                       | <span data-ttu-id="410d3-119">Este é um inteiro que indica o tamanho de cada fatia no quadro em unidades de bits.</span><span class="sxs-lookup"><span data-stu-id="410d3-119">This is an integer that indicates the size of each slice in the frame in units of bits.</span></span> <br/> <span data-ttu-id="410d3-120">O codificador deve iniciar uma nova fatia no macrobloco que faz com que o número de bits na fatia exceda esse valor (portanto, o tamanho de cada fatia sempre será menor ou igual a esse valor).</span><span class="sxs-lookup"><span data-stu-id="410d3-120">The encoder should start a new slice at the macroblock that causes the number of bits in the slice to exceed this value (so the size of each slice will always be less than or equal than this value).</span></span> <span data-ttu-id="410d3-121">Isso significa que o tamanho da última fatia pode ser significativamente menor do que esse valor.</span><span class="sxs-lookup"><span data-stu-id="410d3-121">This means that the last slice size could be significantly smaller than this value.</span></span> <br/> |
| <span data-ttu-id="410d3-122">2</span><span class="sxs-lookup"><span data-stu-id="410d3-122">2</span></span>                                       | <span data-ttu-id="410d3-123">Esse é um inteiro que indica o tamanho de cada fatia no quadro em unidades de macrobloco linhas.</span><span class="sxs-lookup"><span data-stu-id="410d3-123">This is an integer that indicates the size of each slice in the frame in units of macroblock rows.</span></span> <br/> <span data-ttu-id="410d3-124">O codificador deve rejeitar a configuração quando o valor for maior que o número de linhas macrobloco no quadro.</span><span class="sxs-lookup"><span data-stu-id="410d3-124">The encoder should reject the setting when the value is greater than the number of macroblock rows in the frame.</span></span><br/>                                                                                                                                                                 |



 

<span data-ttu-id="410d3-125">Se o aplicativo não definir um valor para [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), o codificador deverá retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="410d3-125">If the application does not set a value for [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), the encoder should return an error.</span></span>

<span data-ttu-id="410d3-126">O padrão recomendado é ter uma única fatia para o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="410d3-126">The recommended default is to have a single slice for whole frame.</span></span>

<span data-ttu-id="410d3-127">Alguns codificadores podem codificar fatias em paralelo e, portanto, o desempenho pode ser afetado dependendo das configurações de controle de fatia.</span><span class="sxs-lookup"><span data-stu-id="410d3-127">Some encoders might encode slices in parallel and so performance could be affected depending on the slice control settings.</span></span> <span data-ttu-id="410d3-128">Por exemplo, codificar um quadro como uma única fatia pode ser mais lento do que se o quadro fosse codificado como várias fatias.</span><span class="sxs-lookup"><span data-stu-id="410d3-128">For example, encoding a frame as a single slice might be slower than if the frame was encoded as multiple slices.</span></span>

<span data-ttu-id="410d3-129">As configurações de controle de fatia são dinâmicas e podem ser alteradas durante a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="410d3-129">The slice control settings are dynamic and can be changed during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="410d3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="410d3-130">Requirements</span></span>



| <span data-ttu-id="410d3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="410d3-131">Requirement</span></span> | <span data-ttu-id="410d3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="410d3-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="410d3-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="410d3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="410d3-134">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="410d3-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="410d3-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="410d3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="410d3-136">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="410d3-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="410d3-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="410d3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="410d3-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="410d3-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410d3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="410d3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410d3-140">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="410d3-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




