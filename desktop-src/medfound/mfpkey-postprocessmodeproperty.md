---
description: Especifica o modo de pós-processamento do decodificador.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: Propriedade MFPKEY_POSTPROCESSMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760654"
---
# <a name="mfpkey_postprocessmode-property"></a><span data-ttu-id="84cfa-103">\_Propriedade CREATEprocessmode do MFPKEY</span><span class="sxs-lookup"><span data-stu-id="84cfa-103">MFPKEY\_POSTPROCESSMODE Property</span></span>

<span data-ttu-id="84cfa-104">Especifica o modo de pós-processamento do decodificador.</span><span class="sxs-lookup"><span data-stu-id="84cfa-104">Specifies the post processing mode for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="84cfa-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="84cfa-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="84cfa-106">**g \_ wszWMVCForcePostProcessMode**</span><span class="sxs-lookup"><span data-stu-id="84cfa-106">**g\_wszWMVCForcePostProcessMode**</span></span>

## <a name="data-type"></a><span data-ttu-id="84cfa-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="84cfa-107">Data Type</span></span>

<span data-ttu-id="84cfa-108">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="84cfa-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="84cfa-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="84cfa-109">Remarks</span></span>

<span data-ttu-id="84cfa-110">Defina essa propriedade como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="84cfa-110">Set this property to one of the following values.</span></span>



| <span data-ttu-id="84cfa-111">Valor</span><span class="sxs-lookup"><span data-stu-id="84cfa-111">Value</span></span> | <span data-ttu-id="84cfa-112">Significado</span><span class="sxs-lookup"><span data-stu-id="84cfa-112">Meaning</span></span>                                                                                |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84cfa-113">-1</span><span class="sxs-lookup"><span data-stu-id="84cfa-113">-1</span></span>    | <span data-ttu-id="84cfa-114">O decodificador define o modo de pós-processamento de maneira adaptável com base nos recursos de CPU disponíveis.</span><span class="sxs-lookup"><span data-stu-id="84cfa-114">The decoder sets the post processing mode adaptively based on available CPU resources.</span></span> |
| <span data-ttu-id="84cfa-115">0</span><span class="sxs-lookup"><span data-stu-id="84cfa-115">0</span></span>     | <span data-ttu-id="84cfa-116">O decodificador não realiza nenhum pós-processamento.</span><span class="sxs-lookup"><span data-stu-id="84cfa-116">The decoder performs no post processing.</span></span>                                               |
| <span data-ttu-id="84cfa-117">1</span><span class="sxs-lookup"><span data-stu-id="84cfa-117">1</span></span>     | <span data-ttu-id="84cfa-118">o decodificador da executa o desbloqueio rápido.</span><span class="sxs-lookup"><span data-stu-id="84cfa-118">fThe decoder performs fast deblocking.</span></span>                                                 |
| <span data-ttu-id="84cfa-119">2</span><span class="sxs-lookup"><span data-stu-id="84cfa-119">2</span></span>     | <span data-ttu-id="84cfa-120">O decodificador executa o desbloqueio completo.</span><span class="sxs-lookup"><span data-stu-id="84cfa-120">The decoder performs full deblocking.</span></span>                                                  |
| <span data-ttu-id="84cfa-121">3</span><span class="sxs-lookup"><span data-stu-id="84cfa-121">3</span></span>     | <span data-ttu-id="84cfa-122">O decodificador executa o desbloqueio e o destoques rápidos.</span><span class="sxs-lookup"><span data-stu-id="84cfa-122">The decoder performs fast deblocking and deringing.</span></span>                                    |
| <span data-ttu-id="84cfa-123">4</span><span class="sxs-lookup"><span data-stu-id="84cfa-123">4</span></span>     | <span data-ttu-id="84cfa-124">O decodificador executa o desbloqueio completo e o destoque.</span><span class="sxs-lookup"><span data-stu-id="84cfa-124">The decoder performs full deblocking and deringing.</span></span>                                    |



 

<span data-ttu-id="84cfa-125">Como o valor dessa propriedade vai de 0 a 4, a complexidade da decodificação, o uso de recursos da CPU e a qualidade da imagem aumentam.</span><span class="sxs-lookup"><span data-stu-id="84cfa-125">As the value of this property goes from 0 to 4, the decoding complexity, use of CPU resources, and picture quality all increase.</span></span>

## <a name="requirements"></a><span data-ttu-id="84cfa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84cfa-126">Requirements</span></span>



| <span data-ttu-id="84cfa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="84cfa-127">Requirement</span></span> | <span data-ttu-id="84cfa-128">Valor</span><span class="sxs-lookup"><span data-stu-id="84cfa-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84cfa-129">Cliente</span><span class="sxs-lookup"><span data-stu-id="84cfa-129">Client</span></span><br/> | <span data-ttu-id="84cfa-130">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="84cfa-130">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="84cfa-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84cfa-131">Header</span></span><br/> | <dl> <span data-ttu-id="84cfa-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="84cfa-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84cfa-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="84cfa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84cfa-134">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84cfa-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




