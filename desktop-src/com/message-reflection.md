---
title: Reflexão de mensagem
description: Reflexão de mensagem
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004839"
---
# <a name="message-reflection"></a><span data-ttu-id="44c46-103">Reflexão de mensagem</span><span class="sxs-lookup"><span data-stu-id="44c46-103">Message Reflection</span></span>

<span data-ttu-id="44c46-104">É altamente recomendável que um contêiner de controle ActiveX dê suporte à reflexão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="44c46-104">It is strongly recommended that an ActiveX control container supports message reflection.</span></span> <span data-ttu-id="44c46-105">Isso resultará em uma operação mais eficiente para controles de subclasse.</span><span class="sxs-lookup"><span data-stu-id="44c46-105">This will result in more efficient operation for subclassed controls.</span></span> <span data-ttu-id="44c46-106">Se a reflexão da mensagem tiver suporte, a propriedade de ambiente MessageReflect deverá ter suporte e ter um valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="44c46-106">If message reflection is supported, the MessageReflect ambient property must be supported and have a value of **TRUE**.</span></span> <span data-ttu-id="44c46-107">Se um contêiner não implementar a reflexão de mensagem, o CDK OLE criará duas janelas para cada controle de subclasse, a fim de fornecer a reflexão de mensagem em nome do contêiner de controle.</span><span class="sxs-lookup"><span data-stu-id="44c46-107">If a container does not implement message reflection, then the OLE CDK creates two windows for every subclassed control, to provide message reflection on behalf on the control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44c46-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44c46-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c46-109">Contêineres</span><span class="sxs-lookup"><span data-stu-id="44c46-109">Containers</span></span>](containers.md)
</dt> </dl>

 

 




