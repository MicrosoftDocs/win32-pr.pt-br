---
title: Como reproduzir uma lista de comandos
description: Este tópico mostra como reproduzir uma lista de comandos.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988513"
---
# <a name="how-to-play-back-a-command-list"></a><span data-ttu-id="24e48-103">Como reproduzir uma lista de comandos</span><span class="sxs-lookup"><span data-stu-id="24e48-103">How to: Play Back a Command List</span></span>

<span data-ttu-id="24e48-104">Uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) é uma lista registrada de comandos de renderização.</span><span class="sxs-lookup"><span data-stu-id="24e48-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="24e48-105">Use uma lista de comandos para gravar previamente os comandos de desenho e reproduzi-los novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="24e48-105">Use a command list to pre-record drawing commands and play them back later.</span></span> <span data-ttu-id="24e48-106">Este tópico mostra como reproduzir uma lista de [comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="24e48-106">This topic shows how to play back a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="24e48-107">Uma lista de comandos pode ser usada para dividir tarefas de renderização entre threads.</span><span class="sxs-lookup"><span data-stu-id="24e48-107">A command list can be used to split rendering tasks between threads.</span></span>

<span data-ttu-id="24e48-108">Esta seção descreve como reproduzir uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="24e48-108">This section describes how to play back a command list.</span></span> <span data-ttu-id="24e48-109">Para gravar uma lista de comandos, consulte [como gravar uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span><span class="sxs-lookup"><span data-stu-id="24e48-109">For recording a command list, see [How to: Record a Command List](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span></span>

<span data-ttu-id="24e48-110">**Para reproduzir uma lista de comandos**</span><span class="sxs-lookup"><span data-stu-id="24e48-110">**To play back a command list**</span></span>

-   <span data-ttu-id="24e48-111">Chame [**ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) e passe um objeto [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) válido.</span><span class="sxs-lookup"><span data-stu-id="24e48-111">Call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) and pass a valid [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) object.</span></span>
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

<span data-ttu-id="24e48-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) deve ser executado no [contexto imediato](overviews-direct3d-11-devices-intro.md) para comandos gravados a serem executados na GPU (unidade de processamento gráfico).</span><span class="sxs-lookup"><span data-stu-id="24e48-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) must be executed on the [immediate context](overviews-direct3d-11-devices-intro.md) for recorded commands to be run on the graphics processing unit (GPU).</span></span> <span data-ttu-id="24e48-113">Use o contexto imediato para alimentar os comandos para a GPU para execução, use um contexto adiado para gravar comandos para reprodução em outra lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="24e48-113">Use the immediate context to feed commands to the GPU for execution, use a deferred context to record commands for playback onto another command list.</span></span> <span data-ttu-id="24e48-114">Ao chamar **ExecuteCommandList** em outro contexto adiado, você cria uma lista de comandos adiados ' mesclados '.</span><span class="sxs-lookup"><span data-stu-id="24e48-114">When you call **ExecuteCommandList** onto another deferred context, you create a ‘merged’ deferred command list.</span></span> <span data-ttu-id="24e48-115">Para executar os comandos na lista de comandos adiados mesclados, você precisa executá-los no contexto imediato.</span><span class="sxs-lookup"><span data-stu-id="24e48-115">To run the commands on the merged deferred command list, you need to execute them on the immediate context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e48-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24e48-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e48-117">Lista de comandos</span><span class="sxs-lookup"><span data-stu-id="24e48-117">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="24e48-118">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="24e48-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




