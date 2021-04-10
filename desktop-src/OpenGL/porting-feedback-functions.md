---
title: Portando funções de comentários
description: Com o íris GL, a maneira como os comentários são tratados difere dependendo do computador que executa o íris GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Portabilidade do íris GL, comentários
- portando do íris GL, comentários
- portando para OpenGL do íris GL, comentários
- Portabilidade do OpenGL do íris GL, comentários
- comentários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160206"
---
# <a name="porting-feedback-functions"></a><span data-ttu-id="373a6-108">Portando funções de comentários</span><span class="sxs-lookup"><span data-stu-id="373a6-108">Porting Feedback Functions</span></span>

<span data-ttu-id="373a6-109">Com o íris GL, a maneira como os comentários são tratados difere dependendo do computador que executa o íris GL.</span><span class="sxs-lookup"><span data-stu-id="373a6-109">With IRIS GL, the way that feedback is handled differs depending on the computer running IRIS GL.</span></span> <span data-ttu-id="373a6-110">O OpenGL padroniza as funções de comentários para que você possa contar com comentários consistentes entre várias plataformas de hardware.</span><span class="sxs-lookup"><span data-stu-id="373a6-110">OpenGL standardizes feedback functions so you can rely on consistent feedback among various hardware platforms.</span></span> <span data-ttu-id="373a6-111">A tabela a seguir lista as funções de comentários da íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="373a6-111">The following table lists the IRIS GL feedback functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="373a6-112">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="373a6-112">IRIS GL function</span></span> | <span data-ttu-id="373a6-113">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="373a6-113">OpenGL function</span></span>                                                                                            | <span data-ttu-id="373a6-114">Significado</span><span class="sxs-lookup"><span data-stu-id="373a6-114">Meaning</span></span>                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="373a6-115">**receber**</span><span class="sxs-lookup"><span data-stu-id="373a6-115">**feedback**</span></span>     | <span data-ttu-id="373a6-116">[**glRenderMode**](glrendermode.md) (comentários do GL \_ )</span><span class="sxs-lookup"><span data-stu-id="373a6-116">[**glRenderMode**](glrendermode.md) ( GL\_FEEDBACK )</span></span>                                                      | <span data-ttu-id="373a6-117">Alterna para o modo de comentários.</span><span class="sxs-lookup"><span data-stu-id="373a6-117">Switches to feedback mode.</span></span>                    |
| <span data-ttu-id="373a6-118">**endfeedback**</span><span class="sxs-lookup"><span data-stu-id="373a6-118">**endfeedback**</span></span>  | <span data-ttu-id="373a6-119">[**glRenderMode**](glrendermode.md) (GL \_ renderizar)[**glFeedbackBuffer**](glfeedbackbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="373a6-119">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span></span><br/> | <span data-ttu-id="373a6-120">Alterna para o modo de renderização.</span><span class="sxs-lookup"><span data-stu-id="373a6-120">Switches to rendering mode.</span></span>                   |
| <span data-ttu-id="373a6-121">**passagem**</span><span class="sxs-lookup"><span data-stu-id="373a6-121">**passthrough**</span></span>  | [<span data-ttu-id="373a6-122">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="373a6-122">**glPassThrough**</span></span>](glpassthrough.md)                                                                     | <span data-ttu-id="373a6-123">Coloca um marcador de token no buffer de comentários.</span><span class="sxs-lookup"><span data-stu-id="373a6-123">Places a token marker in the feedback buffer.</span></span> |



 

 

 





