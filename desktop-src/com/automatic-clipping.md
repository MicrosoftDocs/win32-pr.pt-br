---
title: Recorte automático
description: Recorte automático
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292507"
---
# <a name="automatic-clipping"></a><span data-ttu-id="8561a-103">Recorte automático</span><span class="sxs-lookup"><span data-stu-id="8561a-103">Automatic Clipping</span></span>

<span data-ttu-id="8561a-104">É altamente recomendável que um contêiner de controle ActiveX dê suporte ao recorte automático de seus controles.</span><span class="sxs-lookup"><span data-stu-id="8561a-104">It is strongly recommended that an ActiveX control container supports automatic clipping of its controls.</span></span> <span data-ttu-id="8561a-105">Isso resultará em uma operação mais eficiente para a maioria dos controles.</span><span class="sxs-lookup"><span data-stu-id="8561a-105">This will result in more efficient operation for most controls.</span></span> <span data-ttu-id="8561a-106">Se o recorte automático tiver suporte, a propriedade de ambiente autoclip deve ter suporte e ter um valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="8561a-106">If automatic clipping is supported, the AutoClip ambient property must be supported and have a value of **TRUE**.</span></span>

<span data-ttu-id="8561a-107">O recorte automático é a capacidade de um contêiner de garantir que a saída desenhada de um controle vá apenas para a região de recorte atual do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8561a-107">Automatic clipping is the ability of a container to ensure that a control's drawn output goes only to the container's current clipping region.</span></span> <span data-ttu-id="8561a-108">Em um contêiner que dá suporte a recorte automático, um controle pode pintar sem considerar sua região de recorte, porque o contêiner cortará automaticamente qualquer pintura que ocorra fora da área do controle.</span><span class="sxs-lookup"><span data-stu-id="8561a-108">In a container that supports automatic clipping, a control can paint without regard to its clipping region, because the container will automatically clip any painting that occurs outside the control's area.</span></span> <span data-ttu-id="8561a-109">Se um contêiner não oferecer suporte a recorte automático, os controles gerados pelo CDK criarão uma janela pai extra se uma região de recorte não nula for passada.</span><span class="sxs-lookup"><span data-stu-id="8561a-109">If a container does not support automatic clipping, then CDK-generated controls will create an extra parent window if a non-null clipping region is passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8561a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8561a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8561a-111">Contêineres</span><span class="sxs-lookup"><span data-stu-id="8561a-111">Containers</span></span>](containers.md)
</dt> </dl>

 

 




