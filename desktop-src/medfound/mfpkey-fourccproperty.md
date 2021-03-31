---
description: Especifica o FOURCC que identifica o codificador que você deseja usar.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Propriedade MFPKEY_FOURCC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921399"
---
# <a name="mfpkey_fourcc-property"></a><span data-ttu-id="31c67-103">\_Propriedade FOURCC MFPKEY</span><span class="sxs-lookup"><span data-stu-id="31c67-103">MFPKEY\_FOURCC Property</span></span>

<span data-ttu-id="31c67-104">Especifica o FOURCC que identifica o codificador que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="31c67-104">Specifies the FOURCC that identifies the encoder you want to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="31c67-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="31c67-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="31c67-106">g \_ wszWMVCFOURCC</span><span class="sxs-lookup"><span data-stu-id="31c67-106">g\_wszWMVCFOURCC</span></span>

## <a name="data-type"></a><span data-ttu-id="31c67-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="31c67-107">Data Type</span></span>

<span data-ttu-id="31c67-108">VT \_ i4 (valor FourCC)</span><span class="sxs-lookup"><span data-stu-id="31c67-108">VT\_I4 (FOURCC value)</span></span>

## <a name="remarks"></a><span data-ttu-id="31c67-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="31c67-109">Remarks</span></span>

<span data-ttu-id="31c67-110">Você deve definir esse valor antes de recuperar os valores para as seguintes propriedades usando **IPropertyBag** ou **IPropertyStore**:</span><span class="sxs-lookup"><span data-stu-id="31c67-110">You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:</span></span>

-   [<span data-ttu-id="31c67-111">MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE</span><span class="sxs-lookup"><span data-stu-id="31c67-111">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE</span></span>](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [<span data-ttu-id="31c67-112">MFPKEY \_ PASSESRECOMMENDED</span><span class="sxs-lookup"><span data-stu-id="31c67-112">MFPKEY\_PASSESRECOMMENDED</span></span>](mfpkey-passesrecommendedproperty.md)

<span data-ttu-id="31c67-113">Você deve usar [**IWMCodecProps:: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar os valores das propriedades dependentes de FOURCC listadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="31c67-113">You should use [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) to retrieve the values of the FOURCC-dependent properties listed previously.</span></span> <span data-ttu-id="31c67-114">Ao usar **GetCodecProp**, você não precisa definir **MFPKEY \_ FOURCC**.</span><span class="sxs-lookup"><span data-stu-id="31c67-114">When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.</span></span>

## <a name="requirements"></a><span data-ttu-id="31c67-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31c67-115">Requirements</span></span>



| <span data-ttu-id="31c67-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="31c67-116">Requirement</span></span> | <span data-ttu-id="31c67-117">Valor</span><span class="sxs-lookup"><span data-stu-id="31c67-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31c67-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31c67-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31c67-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31c67-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31c67-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31c67-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31c67-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31c67-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31c67-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31c67-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c67-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31c67-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31c67-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="31c67-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c67-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31c67-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




