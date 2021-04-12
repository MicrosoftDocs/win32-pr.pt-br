---
title: Operações de rede DRM
description: Operações de rede DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- SDK do Windows Media Format, operações de rede DRM
- Formato de sistema avançado (ASF), operações de rede de DRM
- ASF (formato de sistemas avançados), operações de rede de DRM
- DRM (gerenciamento de direitos digitais), operações de rede
- DRM (gerenciamento de direitos digitais), operações de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291862"
---
# <a name="drm-network-operations"></a><span data-ttu-id="2aca0-108">Operações de rede DRM</span><span class="sxs-lookup"><span data-stu-id="2aca0-108">DRM Network Operations</span></span>

<span data-ttu-id="2aca0-109">Várias operações relacionadas ao DRM exigem que seu aplicativo se conecte a um serviço em execução em uma rede.</span><span class="sxs-lookup"><span data-stu-id="2aca0-109">Several DRM-related operations require your application to connect to a service running on a network.</span></span> <span data-ttu-id="2aca0-110">Essas operações incluem individualização, aquisição de licença, revogação de licença e backup e restauração de licenças.</span><span class="sxs-lookup"><span data-stu-id="2aca0-110">These operations include individualization, license acquisition, license revocation, and license backup and restoration.</span></span>

<span data-ttu-id="2aca0-111">Assim como ocorre com qualquer transação de rede, seu aplicativo deve considerar uma variedade de dificuldades ao incluir recursos que exigem operações de rede.</span><span class="sxs-lookup"><span data-stu-id="2aca0-111">As with any network transaction, your application should account for a variety of difficulties when including features that require network operations.</span></span> <span data-ttu-id="2aca0-112">Seu aplicativo deve controlar o status da operação para qualquer extensão possível para o recurso específico, geralmente manipulando mensagens de status.</span><span class="sxs-lookup"><span data-stu-id="2aca0-112">Your application should track the status of the operation to whatever extent is possible for the specific feature, usually by handling status messages.</span></span> <span data-ttu-id="2aca0-113">Você deve fornecer comentários ao usuário sobre o status.</span><span class="sxs-lookup"><span data-stu-id="2aca0-113">You should provide feedback to the user about status.</span></span> <span data-ttu-id="2aca0-114">Se uma operação falhar na primeira tentativa, você deverá dar ao usuário a oportunidade de tentar novamente.</span><span class="sxs-lookup"><span data-stu-id="2aca0-114">If an operation fails on the first try, you should give the user the opportunity to retry.</span></span> <span data-ttu-id="2aca0-115">Em muitos casos, a primeira tentativa encontra dificuldade, mas uma tentativa subsequente é concluída sem erros.</span><span class="sxs-lookup"><span data-stu-id="2aca0-115">In many cases, the first attempt encounters difficulty, but a subsequent try completes without error.</span></span>

> [!Note]  
> <span data-ttu-id="2aca0-116">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="2aca0-116">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2aca0-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2aca0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aca0-118">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="2aca0-118">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




