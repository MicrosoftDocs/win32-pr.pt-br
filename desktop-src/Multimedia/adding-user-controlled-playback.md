---
title: Adicionando User-Controlled reprodução
description: Adicionando User-Controlled reprodução
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105752629"
---
# <a name="adding-user-controlled-playback"></a><span data-ttu-id="69fca-104">Adicionando User-Controlled reprodução</span><span class="sxs-lookup"><span data-stu-id="69fca-104">Adding User-Controlled Playback</span></span>

<span data-ttu-id="69fca-105">Você pode adicionar a reprodução controlada pelo usuário a um aplicativo existente chamando a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="69fca-105">You can add user-controlled playback to an existing application by calling the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function as follows:</span></span>


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



<span data-ttu-id="69fca-106">Os parâmetros [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identificam identificadores para a janela pai e para a instância de módulo associada à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="69fca-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) parameters identify handles to the parent window and to the module instance associated with the MCIWnd window.</span></span> <span data-ttu-id="69fca-107">Eles também especificam estilos de janela e o nome de arquivo (ou nome do dispositivo) a ser associado à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="69fca-107">They also specify window styles and the filename (or device name) to associate with the MCIWnd window.</span></span>

<span data-ttu-id="69fca-108">O **MCIWndCreate** executa automaticamente as seguintes etapas que, para outras classes de janela, você pode implementar em seu código por conta própria:</span><span class="sxs-lookup"><span data-stu-id="69fca-108">**MCIWndCreate** automatically performs the following steps that, for other window classes, you would implement in your code yourself:</span></span>

1.  <span data-ttu-id="69fca-109">Registre a classe da janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="69fca-109">Register the MCIWnd window class.</span></span>
2.  <span data-ttu-id="69fca-110">Crie a janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="69fca-110">Create the MCIWnd window.</span></span>
3.  <span data-ttu-id="69fca-111">Carregar o conteúdo especificado.</span><span class="sxs-lookup"><span data-stu-id="69fca-111">Load the specified content.</span></span>
4.  <span data-ttu-id="69fca-112">Estabeleça a posição de reprodução atual no início do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="69fca-112">Establish the current playback position at the beginning of the content.</span></span>
5.  <span data-ttu-id="69fca-113">Exibir o controle de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69fca-113">Display the device control.</span></span>
6.  <span data-ttu-id="69fca-114">Exiba a área de reprodução da janela, se necessário.</span><span class="sxs-lookup"><span data-stu-id="69fca-114">Display the playback area of the window, if needed.</span></span>

 

 




