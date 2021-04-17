---
description: Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: Atributo MFSampleExtension_ROIRectangle (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762188"
---
# <a name="mfsampleextension_roirectangle-attribute"></a><span data-ttu-id="11d7e-103">\_Atributo MFSampleExtension ROIRectangle</span><span class="sxs-lookup"><span data-stu-id="11d7e-103">MFSampleExtension\_ROIRectangle attribute</span></span>

<span data-ttu-id="11d7e-104">Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.</span><span class="sxs-lookup"><span data-stu-id="11d7e-104">Specifies the bounds of the region of interest which indicates the region of the frame that requires different quality.</span></span>

## <a name="data-type"></a><span data-ttu-id="11d7e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="11d7e-105">Data type</span></span>

<span data-ttu-id="11d7e-106">**[**ROI \_ ÁREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** armazenada como **blob**</span><span class="sxs-lookup"><span data-stu-id="11d7e-106">**[**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stored as **BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="11d7e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="11d7e-107">Remarks</span></span>

<span data-ttu-id="11d7e-108">Depois de configurar com êxito [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) para um valor diferente de zero em um MFT do codificador, o aplicativo pode definir esse atributo em exemplos de entrada e esperar que ele seja respeitado.</span><span class="sxs-lookup"><span data-stu-id="11d7e-108">After successfully setting [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) to a non-zero value on an encoder MFT, the application can set this attribute on input samples and expect it to be honored.</span></span>

<span data-ttu-id="11d7e-109">Se [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) não for definido como um valor diferente de zero, o \_ atributo MFSampleExtension ROIRectangle será ignorado em exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="11d7e-109">If [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) is not set to a non-zero value, the MFSampleExtension\_ROIRectangle attribute is ignored on input samples.</span></span>

<span data-ttu-id="11d7e-110">MFSampleExtension \_ ROIRectangle é definido em um exemplo de entrada e é aplicado somente à amostra de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="11d7e-110">MFSampleExtension\_ROIRectangle is set on an input sample and is only applied to the current input sample.</span></span>

<span data-ttu-id="11d7e-111">O campo **QPDelta** na estrutura [**da \_ área de ROI**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) especifica o Delta de parâmetro de quantificação para a região especificada a partir do restante do quadro.</span><span class="sxs-lookup"><span data-stu-id="11d7e-111">The **QPDelta** field on the [**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) structure specifies the quantization parameter delta for the specified region from the rest of the frame.</span></span> <span data-ttu-id="11d7e-112">Se **QPDelta** for positivo, isso indicará que o aplicativo quer que o retângulo tenha uma qualidade menor do que o restante do quadro.</span><span class="sxs-lookup"><span data-stu-id="11d7e-112">If **QPDelta** is positive, this indicates the application wants the rectangle to have lower quality than the rest of the frame.</span></span>

<span data-ttu-id="11d7e-113">**Codificadores H. 264/AVC:** **QPDelta** deve estar entre \[ -25, + 25 \] .</span><span class="sxs-lookup"><span data-stu-id="11d7e-113">**H.264/AVC encoders:** **QPDelta** shall be between \[-25, +25\].</span></span> <span data-ttu-id="11d7e-114">O codificador deve garantir que a QP final esteja em um intervalo válido para o padrão de vídeo.</span><span class="sxs-lookup"><span data-stu-id="11d7e-114">The encoder shall ensure that the final QP is in a valid range for the video standard.</span></span>

<span data-ttu-id="11d7e-115">A região especificada não precisa ser alinhada em MB.</span><span class="sxs-lookup"><span data-stu-id="11d7e-115">The specified region is not required to be MB aligned.</span></span> <span data-ttu-id="11d7e-116">Os codificadores têm flexibilidade para decidir o limite real.</span><span class="sxs-lookup"><span data-stu-id="11d7e-116">Encoders have flexibility to decide the actual boundary.</span></span> <span data-ttu-id="11d7e-117">É recomendável cobrir toda a região especificada.</span><span class="sxs-lookup"><span data-stu-id="11d7e-117">It is recommended to cover the entire specified region.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d7e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11d7e-118">Requirements</span></span>



| <span data-ttu-id="11d7e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d7e-119">Requirement</span></span> | <span data-ttu-id="11d7e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="11d7e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11d7e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11d7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="11d7e-122">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="11d7e-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="11d7e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11d7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="11d7e-124">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="11d7e-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="11d7e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11d7e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="11d7e-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d7e-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d7e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="11d7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d7e-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11d7e-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




