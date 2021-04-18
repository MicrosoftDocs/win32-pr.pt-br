---
description: Especifica o número de quadros de vídeo codificados pelo codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Propriedade MFPKEY_CODEDFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766931"
---
# <a name="mfpkey_codedframes-property"></a><span data-ttu-id="f5beb-103">\_Propriedade MFPKEY CODEDFRAMES</span><span class="sxs-lookup"><span data-stu-id="f5beb-103">MFPKEY\_CODEDFRAMES Property</span></span>

<span data-ttu-id="f5beb-104">Especifica o número de quadros de vídeo codificados pelo codec.</span><span class="sxs-lookup"><span data-stu-id="f5beb-104">Specifies the number of video frames encoded by the codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f5beb-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f5beb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f5beb-106">g \_ wszWMVCCodedFrames</span><span class="sxs-lookup"><span data-stu-id="f5beb-106">g\_wszWMVCCodedFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="f5beb-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f5beb-107">Data Type</span></span>

<span data-ttu-id="f5beb-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="f5beb-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="f5beb-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5beb-109">Remarks</span></span>

<span data-ttu-id="f5beb-110">Esse valor é igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos quaisquer quadros que foram descartados devido a restrições de taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="f5beb-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints.</span></span> <span data-ttu-id="f5beb-111">Você pode obter esse valor depois de terminar de passar amostras.</span><span class="sxs-lookup"><span data-stu-id="f5beb-111">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5beb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5beb-112">Requirements</span></span>



| <span data-ttu-id="f5beb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5beb-113">Requirement</span></span> | <span data-ttu-id="f5beb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f5beb-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5beb-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5beb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f5beb-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f5beb-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5beb-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5beb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f5beb-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5beb-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5beb-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5beb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5beb-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5beb-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5beb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5beb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5beb-122">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5beb-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




