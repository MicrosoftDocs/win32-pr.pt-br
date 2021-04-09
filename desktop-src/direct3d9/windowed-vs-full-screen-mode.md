---
description: 'Os aplicativos Direct3D podem ser executados em um dos dois modos: tela inteira ou janelas.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modo Window vs Full-Screen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087382"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a><span data-ttu-id="a746e-103">Modo Window vs Full-Screen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a746e-103">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>

<span data-ttu-id="a746e-104">Os aplicativos Direct3D podem ser executados em um dos dois modos: tela inteira ou janelas.</span><span class="sxs-lookup"><span data-stu-id="a746e-104">Direct3D applications can run in either of two modes: full-screen or windowed.</span></span>

<span data-ttu-id="a746e-105">O modo de tela inteira significa que a janela em que o aplicativo é executado cobre toda a área de trabalho, ocultando todos os aplicativos em execução (incluindo o ambiente de desenvolvimento).</span><span class="sxs-lookup"><span data-stu-id="a746e-105">Full-screen mode means the window that the application runs in covers the entire desktop, hiding all running applications (including your development environment).</span></span> <span data-ttu-id="a746e-106">Jogos normalmente usam o modo de tela inteira por padrão para imergir o usuário no jogo, ocultando todos os aplicativos em execução.</span><span class="sxs-lookup"><span data-stu-id="a746e-106">Games typically default to full-screen mode to fully immerse the user in the game by hiding all running applications.</span></span> <span data-ttu-id="a746e-107">Um aplicativo em execução no modo de janela compartilha a área de trabalho com todos os aplicativos em execução.</span><span class="sxs-lookup"><span data-stu-id="a746e-107">An application running in windowed-mode shares the desktop with all running applications.</span></span> <span data-ttu-id="a746e-108">As diferenças de código entre o modo de tela inteira e modo de janela são muito pequenas.</span><span class="sxs-lookup"><span data-stu-id="a746e-108">Code differences between full-screen mode and windowed mode are very small.</span></span>

<span data-ttu-id="a746e-109">Como um aplicativo em execução no modo de tela inteira assume a tela, depurar o aplicativo requer um monitor separado ou o uso de um depurador remoto.</span><span class="sxs-lookup"><span data-stu-id="a746e-109">Because an application running in full-screen mode takes over the screen, debugging the application requires either a separate monitor or the use of a remote debugger.</span></span> <span data-ttu-id="a746e-110">Use a [ferramenta do painel de controle do DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) para habilitar a depuração de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="a746e-110">Use the [DirectX Control Panel Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) to enable multiple-monitor debugging.</span></span> <span data-ttu-id="a746e-111">Uma vantagem de um aplicativo de modo de janela é que você pode percorrer o código em um depurador sem vários monitores ou um depurador remoto.</span><span class="sxs-lookup"><span data-stu-id="a746e-111">One advantage of a windowed-mode application is that you can step through the code in a debugger without multiple monitors or a remote debugger.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a746e-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a746e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a746e-113">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="a746e-113">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 



