---
description: Os aplicativos C++ podem usar testes alfa para controlar quando os pixels são gravados na superfície de destino de renderização.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Estado de teste alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791340"
---
# <a name="alpha-testing-state-direct3d-9"></a><span data-ttu-id="ca0e9-103">Estado de teste alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ca0e9-103">Alpha Testing State (Direct3D 9)</span></span>

<span data-ttu-id="ca0e9-104">Os aplicativos C++ podem usar testes alfa para controlar quando os pixels são gravados na superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-104">C++ applications can use alpha testing to control when pixels are written to the render-target surface.</span></span> <span data-ttu-id="ca0e9-105">Usando o estado de renderização [**D3DRS \_ ALPHATESTENABLE**](./d3drenderstatetype.md) , seu aplicativo define o dispositivo Direct3D atual para que ele teste cada pixel de acordo com uma função de teste alfa.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-105">By using the [**D3DRS\_ALPHATESTENABLE**](./d3drenderstatetype.md) render state, your application sets the current Direct3D device so that it tests each pixel according to an alpha test function.</span></span> <span data-ttu-id="ca0e9-106">Se o teste tiver sucesso, o pixel será gravado na superfície.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-106">If the test succeeds, the pixel is written to the surface.</span></span> <span data-ttu-id="ca0e9-107">Caso contrário, o Direct3D ignora o pixel.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-107">If it does not, Direct3D ignores the pixel.</span></span> <span data-ttu-id="ca0e9-108">Selecione a função de teste alfa com o estado de renderização **D3DRS \_ ALPHAFUNC** .</span><span class="sxs-lookup"><span data-stu-id="ca0e9-108">Select the alpha test function with the **D3DRS\_ALPHAFUNC** render state.</span></span> <span data-ttu-id="ca0e9-109">Seu aplicativo pode definir um valor alfa de referência para todos os pixels para comparar usando o estado de renderização **D3DRS \_ ALPHAREF** .</span><span class="sxs-lookup"><span data-stu-id="ca0e9-109">Your application can set a reference alpha value for all pixels to compare against by using the **D3DRS\_ALPHAREF** render state.</span></span>

<span data-ttu-id="ca0e9-110">O uso mais comum para o teste alfa é melhorar o desempenho ao rasterizar objetos que são quase transparentes.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-110">The most common use for alpha testing is to improve performance when rasterizing objects that are nearly transparent.</span></span> <span data-ttu-id="ca0e9-111">Se os dados de cor que estão sendo rasterizados forem mais opacos do que a cor em um determinado pixel (D3DPCMPCAPS \_ GREATEREQUAL), o pixel será escrito.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-111">If the color data being rasterized is more opaque than the color at a given pixel (D3DPCMPCAPS\_GREATEREQUAL), then the pixel is written.</span></span> <span data-ttu-id="ca0e9-112">Caso contrário, o rasterizador ignora completamente o pixel, salvando o processamento necessário para misturar as duas cores.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-112">Otherwise, the rasterizer ignores the pixel altogether, saving the processing required to blend the two colors.</span></span> <span data-ttu-id="ca0e9-113">O exemplo de código a seguir verifica se uma determinada função de comparação tem suporte e, em caso afirmativo, define os parâmetros da função de comparação necessários para melhorar o desempenho durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-113">The following code example checks if a given comparison function is supported and, if so, it sets the comparison function parameters required to improve performance during rendering.</span></span>


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



<span data-ttu-id="ca0e9-114">Nem todo o hardware dá suporte a todos os recursos de teste alfa.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-114">Not all hardware supports all alpha-testing features.</span></span> <span data-ttu-id="ca0e9-115">Você pode verificar os recursos do dispositivo chamando o método [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ca0e9-115">You can check the device capabilities by calling the [**IDirect3D9::GetDeviceCaps**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ca0e9-116">Depois de recuperar os recursos do dispositivo, verifique o membro AlphaCmpCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associada para a função de comparação desejada.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-116">After retrieving the device capabilities, check the associated [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's AlphaCmpCaps member for the desired comparison function.</span></span> <span data-ttu-id="ca0e9-117">Se o membro AlphaCmpCaps contiver apenas a \_ capacidade do D3DPCMPCAPS Always ou apenas o D3DPCMPCAPS \_ nunca, o driver não oferecerá suporte a testes alfa.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-117">If the AlphaCmpCaps member contains only the D3DPCMPCAPS\_ALWAYS capability or only the D3DPCMPCAPS\_NEVER capability, the driver does not support alpha tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca0e9-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca0e9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca0e9-119">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="ca0e9-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
