---
description: Conjunto de propriedades de revisão do quadro
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propriedades de revisão do quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645934"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="ef8c0-103">Conjunto de propriedades de revisão do quadro</span><span class="sxs-lookup"><span data-stu-id="ef8c0-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="ef8c0-104">Os decodificadores que implementam a busca precisa do quadro no Microsoft DirectShow devem implementar o \_ conjunto de propriedades am KSPROPSETID \_ FrameStep, que é usado em conjunto com a interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .</span><span class="sxs-lookup"><span data-stu-id="ef8c0-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="ef8c0-105">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="ef8c0-105">Property Set GUID</span></span> | <span data-ttu-id="ef8c0-106">\_KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="ef8c0-106">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="ef8c0-107">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="ef8c0-107">Property ID</span></span>                              | <span data-ttu-id="ef8c0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef8c0-108">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8c0-109">\_ \_ etapa FRAMESTEP da propriedade am \_</span><span class="sxs-lookup"><span data-stu-id="ef8c0-109">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="ef8c0-110">Instrui o decodificador a iniciar uma operação de etapa e passa uma estrutura [**\_ \_ FRAMESTEP de propriedade am**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica o número de etapas.</span><span class="sxs-lookup"><span data-stu-id="ef8c0-110">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="ef8c0-111">\_Propriedade am \_ FRAMESTEP \_ cancelar</span><span class="sxs-lookup"><span data-stu-id="ef8c0-111">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="ef8c0-112">Instrui o decodificador para cancelar a operação de etapa atual.</span><span class="sxs-lookup"><span data-stu-id="ef8c0-112">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="ef8c0-113">Nenhum dado de instância está associado a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="ef8c0-113">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="ef8c0-114">\_FRAMESTEP da propriedade am \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef8c0-114">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="ef8c0-115">O decodificador retorna S \_ OK nessa instrução para indicar que ele pode executar a revisão do quadro, \_ caso contrário, S false.</span><span class="sxs-lookup"><span data-stu-id="ef8c0-115">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="ef8c0-116">Nenhum dado de instância é passado quando essa propriedade é definida.</span><span class="sxs-lookup"><span data-stu-id="ef8c0-116">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="ef8c0-117">\_Propriedade am \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="ef8c0-117">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="ef8c0-118">O decodificador retorna S \_ OK nessa instrução para indicar que ele pode passar vários quadros por vez; \_ caso contrário, S false.</span><span class="sxs-lookup"><span data-stu-id="ef8c0-118">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="ef8c0-119">Nenhum dado de instância é passado quando essa propriedade é definida.</span><span class="sxs-lookup"><span data-stu-id="ef8c0-119">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ef8c0-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef8c0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef8c0-121">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="ef8c0-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



