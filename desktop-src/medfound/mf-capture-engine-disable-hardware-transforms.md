---
description: Desabilita o uso de transformações de Media Foundation baseadas em hardware (MFTs) no mecanismo de captura.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Atributo MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798547"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a><span data-ttu-id="0c51b-103">O \_ mecanismo de captura MF \_ desabilita o atributo de \_ \_ \_ transformações de hardware</span><span class="sxs-lookup"><span data-stu-id="0c51b-103">MF\_CAPTURE\_ENGINE\_DISABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="0c51b-104">Desabilita o uso de transformações de Media Foundation baseadas em hardware (MFTs) no mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="0c51b-104">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c51b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0c51b-105">Data type</span></span>

<span data-ttu-id="0c51b-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="0c51b-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0c51b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c51b-107">Remarks</span></span>

<span data-ttu-id="0c51b-108">Por padrão, o mecanismo de captura usa os codificadores de hardware ou codificadores.</span><span class="sxs-lookup"><span data-stu-id="0c51b-108">By default, the capture engine uses hardware decoders or encoders.</span></span> <span data-ttu-id="0c51b-109">Para desabilitar o uso de MFTs de hardware, defina esse atributo como **true** ao criar o mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="0c51b-109">To disable the use of hardware MFTs, set this attribute to **TRUE** when you create the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c51b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c51b-110">Requirements</span></span>



| <span data-ttu-id="0c51b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c51b-111">Requirement</span></span> | <span data-ttu-id="0c51b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0c51b-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c51b-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c51b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0c51b-114">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0c51b-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="0c51b-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c51b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0c51b-116">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0c51b-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c51b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c51b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c51b-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c51b-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c51b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c51b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c51b-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c51b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c51b-121">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="0c51b-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c51b-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="0c51b-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




