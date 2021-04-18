---
description: Especifica o CLSID de um plug-in de pós-processamento para um dispositivo de captura de vídeo.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Atributo MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781635"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a><span data-ttu-id="92925-103">\_ \_ \_ Atributo CLSID de plugin de extensão MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="92925-103">MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute</span></span>

<span data-ttu-id="92925-104">Especifica o CLSID de um plug-in de pós-processamento para um dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="92925-104">Specifies the CLSID of a post-processing plug-in for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="92925-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="92925-105">Data type</span></span>

<span data-ttu-id="92925-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="92925-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="92925-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="92925-107">Remarks</span></span>

<span data-ttu-id="92925-108">Um plug-in de pós-processamento é um MFT que processa a imagem de vídeo depois que ela é capturada.</span><span class="sxs-lookup"><span data-stu-id="92925-108">A post-processing plug-in is an MFT that processes the video image after it is captured.</span></span> <span data-ttu-id="92925-109">O fornecedor de hardware pode incluir um plug-in de pós-processamento como parte do pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="92925-109">The hardware vendor can include a post-processing plug-in as part of the installation package.</span></span> <span data-ttu-id="92925-110">Nesse caso, a fonte de captura de vídeo define \_ o \_ \_ atributo CLSID do plug-in de extensão MF DEVICESTREAM \_ para o CLSID do plug-in.</span><span class="sxs-lookup"><span data-stu-id="92925-110">If so, the video capture source sets the MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute to the CLSID of the plug-in.</span></span>

<span data-ttu-id="92925-111">Para obter esse atributo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="92925-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="92925-112">Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="92925-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="92925-113">Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="92925-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="92925-114">Chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) para obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="92925-114">Call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) to get the attribute.</span></span>

<span data-ttu-id="92925-115">Para criar o plug-in, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="92925-115">To create the plug-in, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="requirements"></a><span data-ttu-id="92925-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92925-116">Requirements</span></span>



| <span data-ttu-id="92925-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="92925-117">Requirement</span></span> | <span data-ttu-id="92925-118">Valor</span><span class="sxs-lookup"><span data-stu-id="92925-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92925-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92925-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92925-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="92925-120">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="92925-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92925-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92925-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="92925-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92925-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92925-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="92925-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92925-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92925-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="92925-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92925-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92925-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
