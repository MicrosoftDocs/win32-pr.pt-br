---
description: Contém um ponteiro para o Gerenciador de Dispositivos DXGI para o gravador do coletor.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Atributo MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798540"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a><span data-ttu-id="f2f6d-103">\_Atributo de \_ Gerenciador de D3D do gravador de coletor MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="f2f6d-103">MF\_SINK\_WRITER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="f2f6d-104">Contém um ponteiro para o Gerenciador de Dispositivos DXGI para o [gravador do coletor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="f2f6d-104">Contains a pointer to the DXGI Device Manager for the [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="f2f6d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f2f6d-105">Data type</span></span>

<span data-ttu-id="f2f6d-106">**IMFDXGIDeviceManager \** _ armazenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="f2f6d-106">**IMFDXGIDeviceManager\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f6d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2f6d-107">Remarks</span></span>

<span data-ttu-id="f2f6d-108">O valor desse atributo é um ponteiro para a interface [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="f2f6d-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="f2f6d-109">Use esse atributo para fornecer um dispositivo Direct3D para qualquer codificador de vídeo ou coletores de mídia carregados pelo gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="f2f6d-109">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the Sink Writer.</span></span>

<span data-ttu-id="f2f6d-110">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="f2f6d-110">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="f2f6d-111">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="f2f6d-111">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="f2f6d-112">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="f2f6d-112">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="f2f6d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f6d-113">Requirements</span></span>



| <span data-ttu-id="f2f6d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f6d-114">Requirement</span></span> | <span data-ttu-id="f2f6d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f2f6d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f6d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2f6d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f6d-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f2f6d-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f2f6d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2f6d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f6d-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f2f6d-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f2f6d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2f6d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f6d-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f6d-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f6d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2f6d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f6d-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2f6d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2f6d-124">Gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="f2f6d-124">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 




