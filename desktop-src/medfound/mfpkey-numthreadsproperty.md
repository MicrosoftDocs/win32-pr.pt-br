---
description: Especifica o número de threads que o codificador usará.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: Propriedade MFPKEY_NUMTHREADS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505731"
---
# <a name="mfpkey_numthreads-property"></a><span data-ttu-id="f09da-103">\_Propriedade MFPKEY NUMTHREADS</span><span class="sxs-lookup"><span data-stu-id="f09da-103">MFPKEY\_NUMTHREADS Property</span></span>

<span data-ttu-id="f09da-104">Especifica o número de threads que o codificador usará.</span><span class="sxs-lookup"><span data-stu-id="f09da-104">Specifies the number of threads that the encoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f09da-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f09da-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f09da-106">g \_ wszWMVCNumThreads</span><span class="sxs-lookup"><span data-stu-id="f09da-106">g\_wszWMVCNumThreads</span></span>

## <a name="data-type"></a><span data-ttu-id="f09da-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f09da-107">Data Type</span></span>

<span data-ttu-id="f09da-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="f09da-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f09da-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f09da-109">Default Value</span></span>

<span data-ttu-id="f09da-110">1</span><span class="sxs-lookup"><span data-stu-id="f09da-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="f09da-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f09da-111">Remarks</span></span>

<span data-ttu-id="f09da-112">Esse valor destina-se a dividir a codificação em vários threads para aproveitar os computadores com vários processadores.</span><span class="sxs-lookup"><span data-stu-id="f09da-112">This value is intended to divide encoding into multiple threads to take advantage of computers with multiple processors.</span></span> <span data-ttu-id="f09da-113">A divisão de tarefas de codificação em vários threads pode causar uma pequena queda na qualidade em comparação com um único thread.</span><span class="sxs-lookup"><span data-stu-id="f09da-113">Splitting encoding tasks into multiple threads can cause a slight decrease in quality as compared to a single thread.</span></span>

<span data-ttu-id="f09da-114">Para o codificador de vídeo (wmvencod.dll) lançado com o Windows XP e o Windows Vista, essa propriedade deve ser definida como 1, 2 ou 4.</span><span class="sxs-lookup"><span data-stu-id="f09da-114">For the video encoder (wmvencod.dll) released with Windows XP and Windows Vista, this property should be set to 1, 2, or 4.</span></span> <span data-ttu-id="f09da-115">Outros valores serão arredondados para baixo.</span><span class="sxs-lookup"><span data-stu-id="f09da-115">Other values will be rounded down.</span></span>

<span data-ttu-id="f09da-116">Para o codificador de vídeo (wmvencod.dll) lançado com o Windows 7, essa propriedade deve ser definida como 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="f09da-116">For the video encoder (wmvencod.dll) released with Windows 7, this property should be set to 1, 2, 4, or 8.</span></span> <span data-ttu-id="f09da-117">Outros valores serão arredondados para baixo.</span><span class="sxs-lookup"><span data-stu-id="f09da-117">Other values will be rounded down.</span></span>

## <a name="requirements"></a><span data-ttu-id="f09da-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f09da-118">Requirements</span></span>



| <span data-ttu-id="f09da-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f09da-119">Requirement</span></span> | <span data-ttu-id="f09da-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f09da-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f09da-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f09da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f09da-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f09da-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f09da-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f09da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f09da-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f09da-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f09da-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f09da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f09da-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f09da-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09da-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f09da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09da-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f09da-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




