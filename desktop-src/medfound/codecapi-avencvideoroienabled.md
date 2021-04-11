---
description: Indica se o \_ atributo MFSampleExtension ROIRectangle definido no exemplo de entrada será respeitado ou não.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: Propriedade CODECAPI_AVEncVideoROIEnabled (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345e6ba27a983be910f0dc0ea5d3db34191bdcb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296160"
---
# <a name="codecapi_avencvideoroienabled-property"></a><span data-ttu-id="f237c-103">\_Propriedade CODECAPI AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="f237c-103">CODECAPI\_AVEncVideoROIEnabled property</span></span>

<span data-ttu-id="f237c-104">Indica se o atributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) definido no exemplo de entrada será respeitado ou não.</span><span class="sxs-lookup"><span data-stu-id="f237c-104">Indicates whether [MFSampleExtension\_ROIRectangle](mfsampleextension-roirectangle.md) attribute set on the input sample will be honored or not.</span></span>

## <a name="data-type"></a><span data-ttu-id="f237c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f237c-105">Data type</span></span>

<span data-ttu-id="f237c-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="f237c-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f237c-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="f237c-107">Property GUID</span></span>

<span data-ttu-id="f237c-108">**CODECAPI \_ AVEncVideoROIEnabled**</span><span class="sxs-lookup"><span data-stu-id="f237c-108">**CODECAPI\_AVEncVideoROIEnabled**</span></span>

## <a name="remarks"></a><span data-ttu-id="f237c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f237c-109">Remarks</span></span>

<span data-ttu-id="f237c-110">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="f237c-110">Default value is 0.</span></span>

<span data-ttu-id="f237c-111">Se um MFT do codificador aceitar um valor diferente de zero, espera-se que o codificador obedeça o atributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) definido no exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f237c-111">If an encoder MFT accepts a non-zero value, it is expected that the encoder will honor the [MFSampleExtension\_ROIRectangle](mfsampleextension-roirectangle.md) attribute set on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="f237c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f237c-112">Requirements</span></span>



| <span data-ttu-id="f237c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f237c-113">Requirement</span></span> | <span data-ttu-id="f237c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f237c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f237c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f237c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f237c-116">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f237c-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="f237c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f237c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f237c-118">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f237c-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f237c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f237c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f237c-120"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f237c-120"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f237c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f237c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f237c-122">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f237c-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




