---
title: Exibindo ou modificando o sinal de música (preterido)
description: Exibindo ou modificando o sinal de música (preterido)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- SDK do Windows Media Format, caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- SDK do Windows Media Format, caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- SDK do Windows Media Format, exibição ou modificação de sinal de música
- DRM (gerenciamento de direitos digitais), exibição ou modificação de sinal de música
- DRM (gerenciamento de direitos digitais), exibição ou modificação de sinal de música
- Caminho de áudio seguro da Microsoft (SAP), exibição de sinal de música ou modificação
- Caminho de áudio seguro (SAP), exibição de sinal de música ou modificação
- SAP (caminho de áudio seguro), exibição ou modificação de sinal de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783669"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a><span data-ttu-id="a5b2a-115">Exibindo ou modificando o sinal de música (preterido)</span><span class="sxs-lookup"><span data-stu-id="a5b2a-115">Viewing or Modifying the Music Signal (deprecated)</span></span>

<span data-ttu-id="a5b2a-116">Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="a5b2a-117">No modelo de caminho de áudio seguro da Microsoft (SAP), os aplicativos não podem modificar música protegida de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-117">In the Microsoft Secure Audio Path (SAP) model, applications cannot modify protected music in any way.</span></span> <span data-ttu-id="a5b2a-118">Por exemplo, quando um aplicativo tenta interceptar um sinal de música, o sinal parece ser um ruído aleatório.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-118">For example, when an application attempts to intercept a music signal, the signal sounds like random noise.</span></span> <span data-ttu-id="a5b2a-119">Como resultado, os aplicativos que normalmente modificam sinais (como um equalizador) não podem alterar o som da música.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-119">As a result, applications that normally modify signals (such as an equalizer) cannot change the sound of the music.</span></span>

<span data-ttu-id="a5b2a-120">Alguns aplicativos simplesmente exibem um sinal de música.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-120">Some applications merely view a music signal.</span></span> <span data-ttu-id="a5b2a-121">Por exemplo, alguns aplicativos exibem luzes piscadas no tempo com o sinal de música, mas não o modificam.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-121">For example, some applications display flashing lights in time with the music signal, but do not modify it.</span></span> <span data-ttu-id="a5b2a-122">Para acomodar aplicativos que exibem sinais, uma pequena parte da música é descriptografada e passada em formato claro com o conteúdo criptografado.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-122">To accommodate applications that view signals, a small part of the music is decrypted and passed in clear form with the encrypted content.</span></span> <span data-ttu-id="a5b2a-123">O sinal resultante é muito ruim (pior do que a qualidade do telefone), mas pode ser suficiente para aplicativos que exibem sinais.</span><span class="sxs-lookup"><span data-stu-id="a5b2a-123">The resulting signal is very poor (worse than telephone quality) but can suffice for applications that view signals.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5b2a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5b2a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b2a-125">**Caminho de áudio seguro da Microsoft**</span><span class="sxs-lookup"><span data-stu-id="a5b2a-125">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




