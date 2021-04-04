---
title: Para definir as configurações de entrada
description: Para definir as configurações de entrada
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- ASF (Advanced Systems Format), configurações de entrada
- ASF (formato de sistemas avançados), configurações de entrada
- perfis, configurações de entrada
- codecs, configurações de entrada
- fluxos, configurações de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917001"
---
# <a name="to-set-input-settings"></a><span data-ttu-id="fd34e-108">Para definir as configurações de entrada</span><span class="sxs-lookup"><span data-stu-id="fd34e-108">To Set Input Settings</span></span>

<span data-ttu-id="fd34e-109">As propriedades básicas de mídia de entrada e mídia de fluxo são definidas pela estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="fd34e-109">The basic properties of input media and stream media are defined by the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="fd34e-110">Para formatos de entrada, as informações de tipo de mídia são definidas pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd34e-110">For input formats, the media type information is set by your application.</span></span> <span data-ttu-id="fd34e-111">Para formatos de fluxo, as informações de tipo de mídia são definidas no perfil que você atribui ao gravador.</span><span class="sxs-lookup"><span data-stu-id="fd34e-111">For stream formats, the media type information is set in the profile you assign to the writer.</span></span> <span data-ttu-id="fd34e-112">Algumas propriedades são independentes do tipo de mídia e devem ser definidas para uma entrada antes do início da gravação.</span><span class="sxs-lookup"><span data-stu-id="fd34e-112">Some properties are independent of media type and must be set for an input before writing begins.</span></span> <span data-ttu-id="fd34e-113">Essas propriedades são recursos de codec e gravador que são independentes do tipo de fluxo e devem ser definidas após o perfil ser atribuído no gravador, mas antes do início da gravação.</span><span class="sxs-lookup"><span data-stu-id="fd34e-113">These properties are codec and writer features that are independent of stream type, and must be set after the profile is assigned in the writer but before writing begins.</span></span>

<span data-ttu-id="fd34e-114">A definição de uma configuração de entrada requer uma chamada para [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="fd34e-114">Setting an input setting requires a call to [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="fd34e-115">Você também pode verificar o valor atual de uma configuração com uma chamada para [**IWMWriterAdvanced2:: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span><span class="sxs-lookup"><span data-stu-id="fd34e-115">You can also check the current value of a setting with a call to [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd34e-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd34e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd34e-117">**Usar perfis com o gravador**</span><span class="sxs-lookup"><span data-stu-id="fd34e-117">**To Use Profiles with the Writer**</span></span>](to-use-profiles-with-the-writer.md)
</dt> <dt>

[<span data-ttu-id="fd34e-118">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="fd34e-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> <dt>

[<span data-ttu-id="fd34e-119">**Gravando fluxos de imagem**</span><span class="sxs-lookup"><span data-stu-id="fd34e-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




