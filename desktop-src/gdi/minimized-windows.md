---
description: O sistema reduz a janela principal de um aplicativo (estilo sobreposto) a uma janela minimizada quando o usuário clica em minimizar no menu janela ou o aplicativo chama a função de janela e especifica um valor como a \_ minimização do SW.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Janelas minimizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661601"
---
# <a name="minimized-windows"></a><span data-ttu-id="dafb7-103">Janelas minimizadas</span><span class="sxs-lookup"><span data-stu-id="dafb7-103">Minimized Windows</span></span>

<span data-ttu-id="dafb7-104">O sistema reduz a janela principal de um aplicativo (estilo sobreposto) a uma janela minimizada quando o usuário clica em minimizar no menu janela ou o aplicativo chama a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) e especifica um valor como a \_ minimização do SW.</span><span class="sxs-lookup"><span data-stu-id="dafb7-104">The system reduces an application's main window (overlapping style) to a minimized window when the user clicks Minimize from the window menu or the application calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function and specifies a value such as SW\_MINIMIZE.</span></span> <span data-ttu-id="dafb7-105">Minimizar uma janela acelera o desempenho do sistema reduzindo a quantidade de trabalho que um aplicativo deve fazer ao atualizar sua janela principal.</span><span class="sxs-lookup"><span data-stu-id="dafb7-105">Minimizing a window speeds up system performance by reducing the amount of work an application must do when updating its main window.</span></span>

<span data-ttu-id="dafb7-106">Para um aplicativo típico, o sistema desenha um ícone, chamado de ícone de classe, quando a janela é minimizada, rotulando o ícone com o nome da janela.</span><span class="sxs-lookup"><span data-stu-id="dafb7-106">For a typical application, the system draws an icon, called the class icon, when the window is minimized, labeling the icon with the name of the window.</span></span> <span data-ttu-id="dafb7-107">O ícone de classe, uma imagem estática que representa o aplicativo, é especificado pelo aplicativo quando registra a classe de janela.</span><span class="sxs-lookup"><span data-stu-id="dafb7-107">The class icon, a static image that represents the application, is specified by the application when it registers the window class.</span></span> <span data-ttu-id="dafb7-108">O aplicativo atribui um identificador ao ícone de classe para o membro **HICON** de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) antes de chamar [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="dafb7-108">The application assigns a handle to the class icon to the **hIcon** member of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) before calling [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="dafb7-109">O aplicativo pode usar a função [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para recuperar o identificador de ícone.</span><span class="sxs-lookup"><span data-stu-id="dafb7-109">The application can use the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to retrieve the icon handle.</span></span>

 

 
