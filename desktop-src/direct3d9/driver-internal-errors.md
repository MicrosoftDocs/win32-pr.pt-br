---
description: No Direct3D 9, o Direct3D permitirá que o driver retorne códigos de erro como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR \_ UNSUPPORTEDCOLORARG para que um aplicativo possa responder a eles.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Erros internos do driver (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087686"
---
# <a name="driver-internal-errors-direct3d-9"></a><span data-ttu-id="f1f77-103">Erros internos do driver (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f1f77-103">Driver Internal Errors (Direct3D 9)</span></span>

<span data-ttu-id="f1f77-104">No Direct3D 9, o Direct3D permitirá que o driver retorne códigos de erro como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR \_ UNSUPPORTEDCOLORARG para que um aplicativo possa responder a eles.</span><span class="sxs-lookup"><span data-stu-id="f1f77-104">In Direct3D 9, Direct3D will allow the driver to return error codes such as E\_OUTOFMEMORY, D3DERR\_OUTOFVIDEOMEMORY, and D3DERR\_UNSUPPORTEDCOLORARG so that an application would be able to respond to them.</span></span> <span data-ttu-id="f1f77-105">No entanto, às vezes, as chamadas à API que geraram esses tipos de retorno são carregadas em um buffer de comando e são armazenadas em lote para serem enviadas para a GPU (consulte [controlar o tempo de execução e otimizações de driver](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="f1f77-105">However, sometimes the API calls that generated these return types get loaded into a command buffer and are batched up to be sent to the GPU (see [Controlling Runtime and Driver Optimizations](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="f1f77-106">Nesse caso, os erros não podem ser retransmitidos para o aplicativo quando a ação precisa ser executada, portanto o código de erro é consumido pelo tempo de execução e uma observação é feita no objeto de dispositivo que isso aconteceu.</span><span class="sxs-lookup"><span data-stu-id="f1f77-106">In this case, the errors cannot be relayed to the application when action needs to be taken, so the error code is consumed by the runtime and a note is made on the device object that this happened.</span></span> <span data-ttu-id="f1f77-107">Posteriormente, quando o aplicativo invoca [**IDirect3DDevice9::P reenviada**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::P reenviada** retornará D3DERR \_ DRIVERINTERNALERROR.</span><span class="sxs-lookup"><span data-stu-id="f1f77-107">Later when the application invokes [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::Present** will return D3DERR\_DRIVERINTERNALERROR.</span></span> <span data-ttu-id="f1f77-108">É por isso que a melhor abordagem a ser tomada por um aplicativo ao receber um D3DERR \_ DRIVERINTERNALERROR da **IDirect3DDevice9::P reenviada** é destruir e recriar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1f77-108">This is why the best approach for an application to take when receiving a D3DERR\_DRIVERINTERNALERROR from **IDirect3DDevice9::Present** is to destroy and recreate the device.</span></span>

<span data-ttu-id="f1f77-109">Se você quiser tentar depurar mais detalhadamente, aqui estão algumas sugestões para tentar descobrir qual chamada à API está gerando o erro:</span><span class="sxs-lookup"><span data-stu-id="f1f77-109">If you want to try to debug further, here are a couple of suggestions for trying to figure out which API call is generating the error:</span></span>

-   <span data-ttu-id="f1f77-110">Como a lista de possíveis valores de retorno não está completa, você pode tentar descobrir qual chamada está falhando ao redor de cada chamada à API como esta:</span><span class="sxs-lookup"><span data-stu-id="f1f77-110">Because the list of possible return values is not complete, you can try to find which call is failing by surrounding each API call like this:</span></span>

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    <span data-ttu-id="f1f77-111">O fluxo de depuração de saída deve mostrar a chamada que está causando o problema.</span><span class="sxs-lookup"><span data-stu-id="f1f77-111">The output debug stream should then show the call that is causing the problem.</span></span>

-   <span data-ttu-id="f1f77-112">Além disso, para fins de depuração, tente chamar [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) imediatamente antes de cada [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para ver se há um problema adicional com o driver de dispositivo (operação sem suporte, combinação inutilizável de formatos de textura, etc).</span><span class="sxs-lookup"><span data-stu-id="f1f77-112">Additionally, for debugging purposes, try calling [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediately before each [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to see if there is an additional problem with the device driver (unsupported operation, unusable combination of texture formats, etc).</span></span>

    > [!Note]  
    > <span data-ttu-id="f1f77-113">[**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) deve ser usado com cuidado e com moderação devido à quantidade de trabalho de validação que o driver precisa executar para retornar uma resposta.</span><span class="sxs-lookup"><span data-stu-id="f1f77-113">[**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) should be used carefully and sparingly because of the amount of validation work the driver needs to perform to return an answer.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="f1f77-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1f77-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1f77-115">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="f1f77-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
