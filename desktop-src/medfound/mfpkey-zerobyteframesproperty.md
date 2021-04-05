---
description: Especifica o número de quadros de vídeo que são ignorados porque eles eram duplicatas de quadros anteriores.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Propriedade MFPKEY_ZEROBYTEFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827546"
---
# <a name="mfpkey_zerobyteframes-property"></a><span data-ttu-id="d7573-103">\_Propriedade MFPKEY ZEROBYTEFRAMES</span><span class="sxs-lookup"><span data-stu-id="d7573-103">MFPKEY\_ZEROBYTEFRAMES Property</span></span>

<span data-ttu-id="d7573-104">Especifica o número de quadros de vídeo que são ignorados porque eles eram duplicatas de quadros anteriores.</span><span class="sxs-lookup"><span data-stu-id="d7573-104">Specifies the number of video frames that are skipped because they were duplicates of previous frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d7573-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d7573-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d7573-106">g \_ wszWMVCZeroByteFrames</span><span class="sxs-lookup"><span data-stu-id="d7573-106">g\_wszWMVCZeroByteFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="d7573-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d7573-107">Data Type</span></span>

<span data-ttu-id="d7573-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="d7573-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="d7573-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7573-109">Remarks</span></span>

<span data-ttu-id="d7573-110">Esse valor não é subtraído do número total de quadros passados ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) ao calcular o número de quadros codificados ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="d7573-110">This value is not subtracted from the total number of frames passed ([MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md)) when calculating the number of encoded frames ([MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md)).</span></span>

<span data-ttu-id="d7573-111">Você pode parar o codec de ignorar quadros duplicados definindo [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="d7573-111">You can stop the codec from skipping duplicate frames by setting [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE.</span></span>

<span data-ttu-id="d7573-112">Você pode obter esse valor depois de terminar de passar amostras.</span><span class="sxs-lookup"><span data-stu-id="d7573-112">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7573-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7573-113">Requirements</span></span>



| <span data-ttu-id="d7573-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7573-114">Requirement</span></span> | <span data-ttu-id="d7573-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d7573-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7573-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7573-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7573-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d7573-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7573-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7573-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7573-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7573-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7573-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7573-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7573-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7573-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7573-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7573-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7573-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7573-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




