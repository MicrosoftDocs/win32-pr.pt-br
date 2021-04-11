---
description: As GUIDs a seguir definem os tipos para o objeto de exclusão mútua para fluxos ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUIDs do tipo de exclusão mútua do ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164222"
---
# <a name="asf-mutual-exclusion-type-guids"></a><span data-ttu-id="e5116-103">GUIDs do tipo de exclusão mútua do ASF</span><span class="sxs-lookup"><span data-stu-id="e5116-103">ASF Mutual Exclusion Type GUIDs</span></span>

<span data-ttu-id="e5116-104">As GUIDs a seguir definem os tipos para o objeto de exclusão mútua para fluxos ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="e5116-104">The following GUIDs define the types for the mutual exclusion object for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="e5116-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e5116-105">Constant</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="e5116-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5116-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <span data-ttu-id="e5116-107"><dt>**\_Linguagem MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="e5116-107"><dt>**MFASFMutexType\_Language**</dt></span></span> </dl>                 | <span data-ttu-id="e5116-108">Os fluxos são mutuamente exclusivos por idioma.</span><span class="sxs-lookup"><span data-stu-id="e5116-108">The streams are mutually exclusive by language.</span></span> <span data-ttu-id="e5116-109">Esse tipo de exclusão mútua é semelhante às faixas de áudio em um DVD.</span><span class="sxs-lookup"><span data-stu-id="e5116-109">This type of mutual exclusion is similar to the audio tracks on a DVD.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <span data-ttu-id="e5116-110"><dt>**\_Taxa de bits MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="e5116-110"><dt>**MFASFMutexType\_Bitrate**</dt></span></span> </dl>                     | <span data-ttu-id="e5116-111">Os fluxos são mutuamente exclusivos por taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="e5116-111">The streams are mutually exclusive by bit rate.</span></span> <span data-ttu-id="e5116-112">Esse tipo de exclusão mútua também é chamado de exclusão de taxa de bits múltipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="e5116-112">This type of mutual exclusion is also called multiple bit rate (MBR) exclusion.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <span data-ttu-id="e5116-113"><dt>**Apresentação do MFASFMutexType \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e5116-113"><dt>**MFASFMutexType\_Presentation**</dt></span></span> </dl> | <span data-ttu-id="e5116-114">Os fluxos são mutuamente exclusivos por apresentação.</span><span class="sxs-lookup"><span data-stu-id="e5116-114">The streams are mutually exclusive by presentation.</span></span> <span data-ttu-id="e5116-115">Esse tipo pode ser usado para muitos cenários, mas só deve ser usado quando o conteúdo é o mesmo, mas usa um formulário diferente.</span><span class="sxs-lookup"><span data-stu-id="e5116-115">This type can be used for many scenarios, but it should only be used when the content is the same but takes a different form.</span></span> <span data-ttu-id="e5116-116">Por exemplo, dois fluxos contendo o mesmo vídeo, um formatado para preencher a tela e o outro, mantendo a proporção de proporção widescreen original, devem ser mutuamente exclusivos com o uso desse tipo.</span><span class="sxs-lookup"><span data-stu-id="e5116-116">For example, two streams containing the same video, one formatted to fill the screen and the other maintaining the original widescreen aspect ratio, should be made mutually exclusive by using this type.</span></span> <span data-ttu-id="e5116-117">Outro exemplo são os fluxos que contêm vídeo da mesma captura de cena de diferentes ângulos.</span><span class="sxs-lookup"><span data-stu-id="e5116-117">Another example is streams containing video of the same scene shot from different angles.</span></span><br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <span data-ttu-id="e5116-118"><dt>**MFASFMutexType \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="e5116-118"><dt>**MFASFMutexType\_Unknown**</dt></span></span> </dl>                     | <span data-ttu-id="e5116-119">Os fluxos são mutuamente exclusivos com base em critérios personalizados.</span><span class="sxs-lookup"><span data-stu-id="e5116-119">The streams are mutually exclusive based on custom criteria.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="e5116-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5116-120">Requirements</span></span>



| <span data-ttu-id="e5116-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5116-121">Requirement</span></span> | <span data-ttu-id="e5116-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e5116-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5116-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5116-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5116-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5116-124">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5116-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5116-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5116-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5116-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e5116-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5116-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5116-128"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5116-128"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5116-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5116-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5116-130">**IMFASFMutualExclusion:: GetType**</span><span class="sxs-lookup"><span data-stu-id="e5116-130">**IMFASFMutualExclusion::GetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[<span data-ttu-id="e5116-131">**IMFASFMutualExclusion:: SetType**</span><span class="sxs-lookup"><span data-stu-id="e5116-131">**IMFASFMutualExclusion::SetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[<span data-ttu-id="e5116-132">Media Foundation constantes</span><span class="sxs-lookup"><span data-stu-id="e5116-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




