---
description: Os métodos de cursor do mouse permitem que o aplicativo especifique um cursor de cor fornecendo uma superfície que contém uma imagem.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Trabalhando com cursores do mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456798"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a><span data-ttu-id="b4137-103">Trabalhando com cursores do mouse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4137-103">Working with Mouse Cursors (Direct3D 9)</span></span>

<span data-ttu-id="b4137-104">Os métodos de cursor do mouse permitem que o aplicativo especifique um cursor de cor fornecendo uma superfície que contém uma imagem.</span><span class="sxs-lookup"><span data-stu-id="b4137-104">The mouse cursor methods enable the application to specify a color cursor by providing a surface that contains an image.</span></span> <span data-ttu-id="b4137-105">O sistema garantirá que esse cursor será atualizado pela metade da taxa de exibição ou mais se a taxa de quadros do aplicativo for lenta.</span><span class="sxs-lookup"><span data-stu-id="b4137-105">The system will ensure that this cursor will be updated at half the display rate or more if the application's frame rate is slow.</span></span> <span data-ttu-id="b4137-106">No entanto, o cursor nunca será atualizado com mais frequência do que a taxa de atualização de exibição.</span><span class="sxs-lookup"><span data-stu-id="b4137-106">However, the cursor will never be updated more frequently than the display refresh rate.</span></span>

<span data-ttu-id="b4137-107">A posição do cursor do mouse está vinculada ao cursor do sistema, adequadamente dimensionada para a resolução espacial do modo de exibição atual, mas pode ser movida explicitamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4137-107">The mouse cursor position is tied to the system cursor, appropriately scaled for the current display mode spatial resolution, but it can be moved explicitly by the application.</span></span> <span data-ttu-id="b4137-108">Isso é análogo ao comportamento do cursor do mouse do sistema com suporte da API do Win32.</span><span class="sxs-lookup"><span data-stu-id="b4137-108">This is analogous to the behavior of the Win32 API - supported system mouse cursor.</span></span> <span data-ttu-id="b4137-109">Para obter mais informações sobre como usar um cursor do mouse em seu aplicativo do Direct3D, consulte os tópicos de referência a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4137-109">For more information about how to use a mouse cursor in your Direct3D application, see the following reference topics.</span></span>

-   [<span data-ttu-id="b4137-110">**IDirect3DDevice9::ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="b4137-110">**IDirect3DDevice9::ShowCursor**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [<span data-ttu-id="b4137-111">**IDirect3DDevice9::SetCursorPosition**</span><span class="sxs-lookup"><span data-stu-id="b4137-111">**IDirect3DDevice9::SetCursorPosition**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [<span data-ttu-id="b4137-112">**IDirect3DDevice9::SetCursorProperties**</span><span class="sxs-lookup"><span data-stu-id="b4137-112">**IDirect3DDevice9::SetCursorProperties**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

<span data-ttu-id="b4137-113">O Direct3D garante que o mouse tenha suporte por implementações de hardware ou pelo tempo de execução do Direct3D que executa operações de transferência acelerada por hardware ao chamar [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="b4137-113">Direct3D ensures that the mouse is supported either by hardware implementations or by the Direct3D run time that performs hardware-accelerated blitting operations when calling [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4137-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4137-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4137-115">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="b4137-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
