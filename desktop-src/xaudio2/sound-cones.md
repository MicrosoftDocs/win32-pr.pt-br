---
description: Um modelo que descreve a intensidade de som orientado.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Cones de som
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814122"
---
# <a name="sound-cones"></a><span data-ttu-id="2ade5-103">Cones de som</span><span class="sxs-lookup"><span data-stu-id="2ade5-103">Sound Cones</span></span>

<span data-ttu-id="2ade5-104">Um modelo que descreve a intensidade de som orientado.</span><span class="sxs-lookup"><span data-stu-id="2ade5-104">A model that describes the loudness of oriented sound.</span></span>

<span data-ttu-id="2ade5-105">Um som sem orientação tem a mesma amplitude em uma determinada distância em todas as direções.</span><span class="sxs-lookup"><span data-stu-id="2ade5-105">A sound with no orientation has the same amplitude at a given distance in all directions.</span></span> <span data-ttu-id="2ade5-106">Um som com uma orientação é mais alto na direção da orientação.</span><span class="sxs-lookup"><span data-stu-id="2ade5-106">A sound with an orientation is loudest in the direction of orientation.</span></span> <span data-ttu-id="2ade5-107">O modelo que descreve a intensidade do som orientado é chamado de cone de som.</span><span class="sxs-lookup"><span data-stu-id="2ade5-107">The model that describes the loudness of the oriented sound is called a sound cone.</span></span> <span data-ttu-id="2ade5-108">Os cones de som são compostos de um cone interno (ou interno) e de um cone externo (ou externo).</span><span class="sxs-lookup"><span data-stu-id="2ade5-108">Sound cones are made up of an inside (or inner) cone and an outside (or outer) cone.</span></span> <span data-ttu-id="2ade5-109">O ângulo de cone externo sempre deve ser igual ou maior que o ângulo de cone interno.</span><span class="sxs-lookup"><span data-stu-id="2ade5-109">The outside cone angle must always be equal to or greater than the inside cone angle.</span></span>

<span data-ttu-id="2ade5-110">Em qualquer ângulo dentro do cone interno, o volume do som é definido como o volume de cone interno.</span><span class="sxs-lookup"><span data-stu-id="2ade5-110">At any angle within the inner cone, the volume of the sound is set to the inner cone volume.</span></span> <span data-ttu-id="2ade5-111">Isso leva em conta o volume básico do buffer, a distância do ouvinte, a orientação do ouvinte, se o ouvinte tiver seu próprio cone e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2ade5-111">This takes into account the basic volume of the buffer, the distance from the listener, the listener's orientation if the listener has its own cone, and so on.</span></span>

<span data-ttu-id="2ade5-112">Em qualquer ângulo fora do cone externo, o volume normal é atenuado por um fator definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2ade5-112">At any angle outside the outer cone, the normal volume is attenuated by a factor set by the application.</span></span> <span data-ttu-id="2ade5-113">O nível de volume do cone externo é expresso como um dimensionador de amplitude linear: 1,0 f representa nenhuma atenuação aplicada ao sinal original, 0,5 f indica uma atenuação de 6 dB e 0,0 f resulta em silêncio.</span><span class="sxs-lookup"><span data-stu-id="2ade5-113">The outside cone volume level is expressed as a linear amplitude scaler: 1.0 f represents no attenuation applied to the original signal, 0.5 f denotes an attenuation of 6 dB, and 0.0 f results in silence.</span></span> <span data-ttu-id="2ade5-114">A amplificação (volume > 1,0 f) também é permitida e não é clamped.</span><span class="sxs-lookup"><span data-stu-id="2ade5-114">Amplification (volume > 1.0 f) is also allowed, and is not clamped.</span></span> <span data-ttu-id="2ade5-115">O intervalo de volume válido é de, na verdade, 0,0 f a 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="2ade5-115">The valid volume range is actually 0.0 f to 2.0 f.</span></span>

<span data-ttu-id="2ade5-116">Entre o cones interno e o externo está uma zona de transição do volume interno para o volume externo.</span><span class="sxs-lookup"><span data-stu-id="2ade5-116">Between the inner and outer cones is a zone of transition from the inside volume to the outside volume.</span></span> <span data-ttu-id="2ade5-117">O volume se aproxima do volume externo do cone conforme o ângulo aumenta.</span><span class="sxs-lookup"><span data-stu-id="2ade5-117">The volume approaches the cone's outer volume as the angle increases.</span></span>

<span data-ttu-id="2ade5-118">Cones pode afetar parâmetros diferentes de volume.</span><span class="sxs-lookup"><span data-stu-id="2ade5-118">Cones can affect parameters other than volume.</span></span> <span data-ttu-id="2ade5-119">O nível de envio de filtro e reverberação de baixa aprovação também pode ser afetado, tornando a técnica ainda mais dramática.</span><span class="sxs-lookup"><span data-stu-id="2ade5-119">Low pass filter and reverb send level may also be affected, making the technique even more dramatic.</span></span> <span data-ttu-id="2ade5-120">Por exemplo, com um cone no ouvinte, é possível especificar todos os sons por trás do ouvinte, obter um pouco de muffled e ter um conteúdo de taxa de reverberação um pouco maior.</span><span class="sxs-lookup"><span data-stu-id="2ade5-120">For example, with a cone on the listener, one can specify all sounds behind the listener get a bit muffled, and have slightly higher reverb-to-direct ratio content.</span></span> <span data-ttu-id="2ade5-121">Eles fornecem mais indicações de que o som está atrás do usuário.</span><span class="sxs-lookup"><span data-stu-id="2ade5-121">These provide more cues that the sound is behind the user.</span></span> <span data-ttu-id="2ade5-122">Isso melhora o realm.</span><span class="sxs-lookup"><span data-stu-id="2ade5-122">This enhances realism.</span></span>

<span data-ttu-id="2ade5-123">A ilustração a seguir mostra o conceito de cones de som.</span><span class="sxs-lookup"><span data-stu-id="2ade5-123">The following illustration shows the concept of sound cones.</span></span>

![cones de som](images/common-audio-concepts-sound-cones.png)

<span data-ttu-id="2ade5-125">A criação de som cones corretamente pode adicionar efeitos consideráveis ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2ade5-125">Designing sound cones properly can add dramatic effects to your application.</span></span> <span data-ttu-id="2ade5-126">Por exemplo, você pode posicionar uma fonte de som no centro de uma sala, definindo sua orientação em direção a uma porta aberta em um corredor.</span><span class="sxs-lookup"><span data-stu-id="2ade5-126">For example, you could position a sound source in the center of a room, setting its orientation toward an open door in a hallway.</span></span> <span data-ttu-id="2ade5-127">Em seguida, defina o ângulo do cone interior para que ele se estenda para a largura do porta, torne o cone horizontal um pouco mais largo e, por fim, defina o volume do cone externo como inaudível.</span><span class="sxs-lookup"><span data-stu-id="2ade5-127">Then set the angle of the inside cone so that it extends to the width of the doorway, make the outside cone a bit wider, and finally set the outside cone volume to inaudible.</span></span> <span data-ttu-id="2ade5-128">Um ouvinte se mover ao longo do corredor começará a ouvir o som somente quando estiver próximo do porta.</span><span class="sxs-lookup"><span data-stu-id="2ade5-128">A listener moving along the hallway will begin to hear the sound only when near the doorway.</span></span> <span data-ttu-id="2ade5-129">O som será mais alto quando o ouvinte passar na frente da porta aberta.</span><span class="sxs-lookup"><span data-stu-id="2ade5-129">The sound will be loudest as the listener passes in front of the open door.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ade5-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ade5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ade5-131">Conceitos comuns de áudio</span><span class="sxs-lookup"><span data-stu-id="2ade5-131">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="2ade5-132">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="2ade5-132">X3DAudio</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="2ade5-133">**\_Cone X3DAUDIO**</span><span class="sxs-lookup"><span data-stu-id="2ade5-133">**X3DAUDIO\_CONE**</span></span>](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



