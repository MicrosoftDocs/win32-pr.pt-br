---
description: Dois tipos de terminais de faixa são definidos para gravar o terminal de faixa de reprodução e a faixa de execução que, respectivamente, pertencem a e são gerenciados pelo terminal de gravação de arquivos e terminais de reprodução de arquivo.
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Acompanhar terminais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789446"
---
# <a name="track-terminals"></a><span data-ttu-id="e0935-103">Acompanhar terminais</span><span class="sxs-lookup"><span data-stu-id="e0935-103">Track Terminals</span></span>

<span data-ttu-id="e0935-104">Dois tipos de terminais de faixa são definidos: gravação de terminal de faixa de terminais e reprodução de faixa, que, respectivamente, pertence a e é gerenciado por registro de arquivo terminal e terminal de reprodução de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e0935-104">Two types of track terminals are defined: Recording Track Terminal and Playback Track Terminal, which, respectively, belong to and are managed by File Recording Terminal and File Playback Terminal.</span></span>

<span data-ttu-id="e0935-105">Todos os terminais de faixa expõem as interfaces [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) e [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="e0935-105">All track terminals expose the [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) and [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interfaces.</span></span> <span data-ttu-id="e0935-106">A interface **ITTerminal** permite a seleção de terminais de faixa em fluxos ou chamadas.</span><span class="sxs-lookup"><span data-stu-id="e0935-106">The **ITTerminal** interface allows the selection of track terminals onto streams or calls.</span></span>

> [!Note]  
> <span data-ttu-id="e0935-107">Os terminais de faixa também expõem uma interface privada, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), que o MSP usa.</span><span class="sxs-lookup"><span data-stu-id="e0935-107">Track terminals also expose a private interface, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), which the MSP uses.</span></span> <span data-ttu-id="e0935-108">Os aplicativos não devem tentar acessar essa interface.</span><span class="sxs-lookup"><span data-stu-id="e0935-108">Applications should not attempt to access this interface.</span></span>

 

 

 
