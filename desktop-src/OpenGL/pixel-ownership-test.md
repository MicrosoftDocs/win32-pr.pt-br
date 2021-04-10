---
title: Teste de propriedade de pixel
description: O teste de propriedade de pixel determina se o contexto OpenGL atual possui o pixel no framebuffer correspondente a um fragmento específico.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline de processamento de OpenGL, teste de propriedade de pixel
- OpenGL de teste de propriedade de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292337"
---
# <a name="pixel-ownership-test"></a><span data-ttu-id="8205d-105">Teste de propriedade de pixel</span><span class="sxs-lookup"><span data-stu-id="8205d-105">Pixel Ownership Test</span></span>

<span data-ttu-id="8205d-106">O teste de propriedade de pixel determina se o contexto OpenGL atual possui o pixel no framebuffer correspondente a um fragmento específico.</span><span class="sxs-lookup"><span data-stu-id="8205d-106">The pixel ownership test determines whether the current OpenGL context owns the pixel in the framebuffer corresponding to a particular fragment.</span></span> <span data-ttu-id="8205d-107">Nesse caso, o fragmento prossegue para o próximo teste.</span><span class="sxs-lookup"><span data-stu-id="8205d-107">If so, the fragment proceeds to the next test.</span></span> <span data-ttu-id="8205d-108">Caso contrário, o sistema de janelas determinará se o fragmento será descartado ou se outras operações de fragmento serão executadas com esse fragmento.</span><span class="sxs-lookup"><span data-stu-id="8205d-108">If not, the window system determines whether the fragment is discarded or whether any further fragment operations will be performed with that fragment.</span></span> <span data-ttu-id="8205d-109">Com esse teste, o sistema de janelas controla o comportamento quando, por exemplo, uma janela OpenGL é obscurecida.</span><span class="sxs-lookup"><span data-stu-id="8205d-109">With this test, the window system controls behavior when, for example, an OpenGL window is obscured.</span></span>

 

 




