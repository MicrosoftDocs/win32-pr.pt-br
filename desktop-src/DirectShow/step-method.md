---
description: O método step avança o DVD-Video fluxo pelo número especificado de quadros.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Método Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789678"
---
# <a name="step-method"></a><span data-ttu-id="09f9e-103">Método Step</span><span class="sxs-lookup"><span data-stu-id="09f9e-103">Step Method</span></span>

> [!Note]  
> <span data-ttu-id="09f9e-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="09f9e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="09f9e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="09f9e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="09f9e-106">O `Step` método avança o DVD-Video fluxo pelo número especificado de quadros.</span><span class="sxs-lookup"><span data-stu-id="09f9e-106">The `Step` method advances the DVD-Video stream by the specified number of frames.</span></span>

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a><span data-ttu-id="09f9e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09f9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f9e-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="09f9e-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="09f9e-109">Especifica o número de quadros para a etapa como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="09f9e-109">Specifies the number of frames to step as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f9e-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="09f9e-110">Return Value</span></span>

<span data-ttu-id="09f9e-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="09f9e-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09f9e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="09f9e-112">Remarks</span></span>

<span data-ttu-id="09f9e-113">Antes de chamar esse método, chame [**canstep**](canstep-method.md) para determinar se o decodificador dá suporte à revisão de quadros.</span><span class="sxs-lookup"><span data-stu-id="09f9e-113">Before calling this method, call [**CanStep**](canstep-method.md) to determine whether the decoder supports frame stepping.</span></span>

<span data-ttu-id="09f9e-114">Se o DVD-Video estiver sendo executado no modo reverso quando esse método for chamado e o decodificador der suporte à revisão de quadro reverso, a etapa do quadro será feita em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="09f9e-114">If the DVD-Video is playing in reverse mode when this method is called, and the decoder supports reverse frame stepping, then the frame stepping is done in reverse.</span></span>

 

 



