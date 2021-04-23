---
description: Conjunto de propriedades de revisão do quadro
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propriedades de revisão do quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908444"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="e8dff-103">Conjunto de propriedades de revisão do quadro</span><span class="sxs-lookup"><span data-stu-id="e8dff-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="e8dff-104">Os decodificadores que implementam a busca precisa do quadro no Microsoft DirectShow devem implementar o \_ conjunto de propriedades am KSPROPSETID \_ FrameStep, que é usado em conjunto com a interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .</span><span class="sxs-lookup"><span data-stu-id="e8dff-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



| <span data-ttu-id="e8dff-105">Label</span><span class="sxs-lookup"><span data-stu-id="e8dff-105">Label</span></span> | <span data-ttu-id="e8dff-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e8dff-106">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="e8dff-107">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="e8dff-107">Property Set GUID</span></span> | <span data-ttu-id="e8dff-108">\_KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="e8dff-108">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="e8dff-109">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="e8dff-109">Property ID</span></span>                              | <span data-ttu-id="e8dff-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8dff-110">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8dff-111">\_ \_ etapa FRAMESTEP da propriedade am \_</span><span class="sxs-lookup"><span data-stu-id="e8dff-111">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="e8dff-112">Instrui o decodificador a iniciar uma operação de etapa e passa uma estrutura [**\_ \_ FRAMESTEP de propriedade am**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica o número de etapas.</span><span class="sxs-lookup"><span data-stu-id="e8dff-112">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="e8dff-113">\_Propriedade am \_ FRAMESTEP \_ cancelar</span><span class="sxs-lookup"><span data-stu-id="e8dff-113">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="e8dff-114">Instrui o decodificador para cancelar a operação de etapa atual.</span><span class="sxs-lookup"><span data-stu-id="e8dff-114">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="e8dff-115">Nenhum dado de instância está associado a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="e8dff-115">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="e8dff-116">\_FRAMESTEP da propriedade am \_ \_</span><span class="sxs-lookup"><span data-stu-id="e8dff-116">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="e8dff-117">O decodificador retorna S \_ OK nessa instrução para indicar que ele pode executar a revisão do quadro, \_ caso contrário, S false.</span><span class="sxs-lookup"><span data-stu-id="e8dff-117">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="e8dff-118">Nenhum dado de instância é passado quando essa propriedade é definida.</span><span class="sxs-lookup"><span data-stu-id="e8dff-118">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="e8dff-119">\_Propriedade am \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="e8dff-119">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="e8dff-120">O decodificador retorna S \_ OK nessa instrução para indicar que ele pode passar vários quadros por vez; \_ caso contrário, S false.</span><span class="sxs-lookup"><span data-stu-id="e8dff-120">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="e8dff-121">Nenhum dado de instância é passado quando essa propriedade é definida.</span><span class="sxs-lookup"><span data-stu-id="e8dff-121">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e8dff-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8dff-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8dff-123">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="e8dff-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



