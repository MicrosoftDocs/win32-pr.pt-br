---
description: Especifica que o codificador MFT dá suporte ao recebimento de eventos MEEncodingParameter durante o streaming.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Atributo MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754453"
---
# <a name="mft_encoder_supports_config_event-attribute"></a><span data-ttu-id="95fd7-103">O \_ codificador MFT \_ dá suporte ao \_ \_ atributo de evento config</span><span class="sxs-lookup"><span data-stu-id="95fd7-103">MFT\_ENCODER\_SUPPORTS\_CONFIG\_EVENT attribute</span></span>

<span data-ttu-id="95fd7-104">Especifica que o codificador MFT dá suporte ao recebimento de eventos [MEEncodingParameter](meencodingparameters.md) durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="95fd7-104">Specifies that the MFT encoder supports receiving [MEEncodingParameter](meencodingparameters.md) events while streaming.</span></span>

## <a name="data-type"></a><span data-ttu-id="95fd7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="95fd7-105">Data type</span></span>

<span data-ttu-id="95fd7-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="95fd7-106">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="95fd7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="95fd7-107">Remarks</span></span>

<span data-ttu-id="95fd7-108">Enviado pelo codificador MFT por meio de [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="95fd7-108">Sent by the MFT encoder through [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="95fd7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95fd7-109">Requirements</span></span>



| <span data-ttu-id="95fd7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="95fd7-110">Requirement</span></span> | <span data-ttu-id="95fd7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="95fd7-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fd7-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95fd7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="95fd7-113">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="95fd7-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="95fd7-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95fd7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="95fd7-115">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="95fd7-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="95fd7-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95fd7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="95fd7-117"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="95fd7-117"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="95fd7-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="95fd7-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95fd7-119"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95fd7-119"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95fd7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="95fd7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95fd7-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95fd7-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="95fd7-122">**IMFTransform::P rocessEvent**</span><span class="sxs-lookup"><span data-stu-id="95fd7-122">**IMFTransform::ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




