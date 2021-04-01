---
description: Especifica uma janela para que o mecanismo de mídia aplique as proteções do Gerenciador de proteção de saída (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Atributo MF_MEDIA_ENGINE_OPM_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930121"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a><span data-ttu-id="eed4e-103">\_ \_ \_ Atributo HWND de OPM do mecanismo de mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="eed4e-103">MF\_MEDIA\_ENGINE\_OPM\_HWND attribute</span></span>

<span data-ttu-id="eed4e-104">Especifica uma janela para que o mecanismo de mídia aplique as proteções do [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="eed4e-104">Specifies a window for the Media Engine to apply [Output Protection Manager](output-protection-manager.md) (OPM) protections.</span></span>

## <a name="data-type"></a><span data-ttu-id="eed4e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="eed4e-105">Data type</span></span>

<span data-ttu-id="eed4e-106">**HWND** armazenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="eed4e-106">**HWND** stored as **UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="eed4e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="eed4e-107">Remarks</span></span>

<span data-ttu-id="eed4e-108">Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="eed4e-108">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="eed4e-109">Para habilitar as proteções de OPM para reprodução de vídeo, o aplicativo deve executar um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="eed4e-109">To enable OPM protections for video playback, the application must do one of the following:</span></span>

-   <span data-ttu-id="eed4e-110">Defina o [atributo \_ \_ HWND de \_ reprodução \_ do mecanismo de mídia MF](mf-media-engine-playback-hwnd.md) ao criar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="eed4e-110">Set the [MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND](mf-media-engine-playback-hwnd.md) attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="eed4e-111">Defina o \_ atributo HWND do mecanismo de mídia MF \_ \_ \_ para criar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="eed4e-111">Set the MF\_MEDIA\_ENGINE\_OPM\_HWND attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="eed4e-112">Chame [**IMFMediaEngineProtectedContent:: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) em qualquer ponto depois de criar o mecanismo de mídia, mas antes que o conteúdo protegido seja exibido.</span><span class="sxs-lookup"><span data-stu-id="eed4e-112">Call [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) at any point after creating the Media Engine, but before protected content is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed4e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed4e-113">Requirements</span></span>



| <span data-ttu-id="eed4e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed4e-114">Requirement</span></span> | <span data-ttu-id="eed4e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eed4e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed4e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eed4e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eed4e-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="eed4e-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="eed4e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eed4e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eed4e-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="eed4e-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="eed4e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eed4e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eed4e-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="eed4e-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed4e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="eed4e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed4e-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eed4e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eed4e-124">Atributos do mecanismo de mídia</span><span class="sxs-lookup"><span data-stu-id="eed4e-124">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> </dl>

 

 




