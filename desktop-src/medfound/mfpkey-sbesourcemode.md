---
description: Define a configuração de fluxo para a origem de mídia WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: Propriedade MFPKEY_SBESourceMode (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921393"
---
# <a name="mfpkey_sbesourcemode-property"></a><span data-ttu-id="1bbc7-103">\_Propriedade MFPKEY SBESourceMode</span><span class="sxs-lookup"><span data-stu-id="1bbc7-103">MFPKEY\_SBESourceMode property</span></span>

<span data-ttu-id="1bbc7-104">Define a configuração de fluxo para a origem de mídia WTV.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-104">Sets the stream configuration for the WTV media source.</span></span>



<span data-ttu-id="1bbc7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1bbc7-105">Data type</span></span>

<span data-ttu-id="1bbc7-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1bbc7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1bbc7-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1bbc7-107">PROPVARIANT member</span></span>

<span data-ttu-id="1bbc7-108">**INT**</span><span class="sxs-lookup"><span data-stu-id="1bbc7-108">**INT**</span></span>

<span data-ttu-id="1bbc7-109">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="1bbc7-109">VT\_INT</span></span>

<span data-ttu-id="1bbc7-110">**intVal**</span><span class="sxs-lookup"><span data-stu-id="1bbc7-110">**intVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1bbc7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bbc7-111">Remarks</span></span>

<span data-ttu-id="1bbc7-112">Use essa propriedade para configurar a origem da mídia WTV.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-112">Use this property to configure the WTV media source.</span></span> <span data-ttu-id="1bbc7-113">Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="1bbc7-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1bbc7-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1bbc7-115">A origem de mídia do WTV lê arquivos de TV gravados do Windows (. wtv e. ms-drv).</span><span class="sxs-lookup"><span data-stu-id="1bbc7-115">The WTV media source reads Windows Recorded TV Show (.wtv and .ms-drv) files.</span></span>

<span data-ttu-id="1bbc7-116">Essa propriedade deve ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-116">This property must have one of the following values.</span></span>

-   <span data-ttu-id="1bbc7-117">1: mapear os fluxos de áudio disponíveis para uma única saída, com base no local do sistema.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-117">1: Map available audio streams to a single output, based on the system local.</span></span> <span data-ttu-id="1bbc7-118">Esse modo é apropriado para reprodução.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-118">This mode is appropriate for playback.</span></span> <span data-ttu-id="1bbc7-119">(Padrão.)</span><span class="sxs-lookup"><span data-stu-id="1bbc7-119">(Default.)</span></span>
-   2. <span data-ttu-id="1bbc7-120">Todos os fluxos de áudio e subfluxos (como a legenda e os fluxos de dados) são selecionados.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-120">All audio streams and substreams (such as caption and data streams) are selected.</span></span> <span data-ttu-id="1bbc7-121">Esse modo é apropriado para remuxing ou transcodificação.</span><span class="sxs-lookup"><span data-stu-id="1bbc7-121">This mode is appropriate for remuxing or transcoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bbc7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bbc7-122">Requirements</span></span>



| <span data-ttu-id="1bbc7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bbc7-123">Requirement</span></span> | <span data-ttu-id="1bbc7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1bbc7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1bbc7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bbc7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1bbc7-126">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1bbc7-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1bbc7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bbc7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1bbc7-128">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1bbc7-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1bbc7-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bbc7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bbc7-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bbc7-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bbc7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bbc7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bbc7-132">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1bbc7-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
