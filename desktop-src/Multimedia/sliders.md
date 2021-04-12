---
title: Controles deslizantes (multimídia do Windows)
description: Controles deslizantes
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mixers de áudio, controles
- mixers de áudio, controles deslizantes
- mixers, controles
- mixers, controles deslizantes
- controles deslizantes
- Estrutura de MIXERCONTROLDETAILS_SIGNED
- controle panorâmico
- Controle de Pan QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369102"
---
# <a name="sliders-windows-multimedia"></a><span data-ttu-id="eb9c1-111">Controles deslizantes (multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="eb9c1-111">Sliders (Windows Multimedia)</span></span>

<span data-ttu-id="eb9c1-112">Os controles deslizantes geralmente são controles horizontais que podem ser ajustados para a esquerda ou para a direita.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-112">The slider controls are typically horizontal controls that can be adjusted to the left or right.</span></span> <span data-ttu-id="eb9c1-113">Esses controles usam a [**estrutura \_ assinada MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) para recuperar e definir propriedades de controle.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-113">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="eb9c1-114">A tabela a seguir descreve os tipos de controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-114">The following table describes the types of sliders.</span></span>



| <span data-ttu-id="eb9c1-115">Control</span><span class="sxs-lookup"><span data-stu-id="eb9c1-115">Control</span></span>    | <span data-ttu-id="eb9c1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb9c1-116">Description</span></span>                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9c1-117">Controle deslizante</span><span class="sxs-lookup"><span data-stu-id="eb9c1-117">Slider</span></span>     | <span data-ttu-id="eb9c1-118">Tem um intervalo de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-118">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="eb9c1-119">O driver do mixer define os limites deste controle.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-119">The mixer driver defines the limits of this control.</span></span>                               |
| <span data-ttu-id="eb9c1-120">Panorâmica</span><span class="sxs-lookup"><span data-stu-id="eb9c1-120">Pan</span></span>        | <span data-ttu-id="eb9c1-121">Tem um intervalo de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-121">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="eb9c1-122">O driver do mixer define os limites desse controle, com 0 como o valor de midrange.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-122">The mixer driver defines the limits of this control, with 0 as the midrange value.</span></span> |
| <span data-ttu-id="eb9c1-123">Pan QSound</span><span class="sxs-lookup"><span data-stu-id="eb9c1-123">QSound Pan</span></span> | <span data-ttu-id="eb9c1-124">Fornece controle de som expandido por meio de QSound.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-124">Provides expanded sound control through QSound.</span></span> <span data-ttu-id="eb9c1-125">Esse controle tem um intervalo de – 15 a 15.</span><span class="sxs-lookup"><span data-stu-id="eb9c1-125">This control has a range of –15 through 15.</span></span>                               |



 

 

 
