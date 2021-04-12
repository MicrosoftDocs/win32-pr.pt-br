---
title: Portando para OpenGL
description: Portando para OpenGL
ms.assetid: 6799e10b-2f7c-4516-92ea-43667784f8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8efd2a34ac5d7fb6fc52aef3f24a556712b2c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364168"
---
# <a name="porting-to-opengl"></a><span data-ttu-id="545a4-103">Portando para OpenGL</span><span class="sxs-lookup"><span data-stu-id="545a4-103">Porting to OpenGL</span></span>

<span data-ttu-id="545a4-104">O OpenGL foi projetado para compatibilidade entre hardware e sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="545a4-104">OpenGL is designed for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="545a4-105">Esse design torna mais fácil para os programadores portarem programas OpenGL de um sistema para outro.</span><span class="sxs-lookup"><span data-stu-id="545a4-105">This design makes it easier for programmers to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="545a4-106">Embora cada sistema operacional tenha requisitos exclusivos, grande parte do código OpenGL em seus programas atuais pode ser usada como está.</span><span class="sxs-lookup"><span data-stu-id="545a4-106">While each operating system has unique requirements, much of the OpenGL code in your current programs can be used as is.</span></span> <span data-ttu-id="545a4-107">Para portar seu aplicativo OpenGL para o Microsoft Windows, você precisará modificar seus programas para trabalhar com os sistemas de janelas do Windows.</span><span class="sxs-lookup"><span data-stu-id="545a4-107">To port your OpenGL application to Microsoft Windows, you'll have to modify your programs to work with the Windows windowing systems.</span></span>

<span data-ttu-id="545a4-108">Em geral, os aplicativos são portados para o OpenGL para Windows de uma das duas plataformas:</span><span class="sxs-lookup"><span data-stu-id="545a4-108">In general applications are ported to OpenGL for Windows from one of two platforms:</span></span>

-   <span data-ttu-id="545a4-109">Aplicativos OpenGL desenvolvidos para o sistema de janelas X e a biblioteca X (Xlib)</span><span class="sxs-lookup"><span data-stu-id="545a4-109">OpenGL applications developed for the X Window System and the X library (Xlib)</span></span>
-   <span data-ttu-id="545a4-110">Aplicativos da íris GL</span><span class="sxs-lookup"><span data-stu-id="545a4-110">IRIS GL applications</span></span>

<span data-ttu-id="545a4-111">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="545a4-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="545a4-112">Introdução à portabilidade para OpenGL para Windows</span><span class="sxs-lookup"><span data-stu-id="545a4-112">Introduction to Porting to OpenGL for Windows</span></span>](introduction-to-porting-to-opengl-for-windows-nt--windows-2000--and-windows-95-98.md)
-   [<span data-ttu-id="545a4-113">Funções OpenGL e seus equivalentes do íris GL</span><span class="sxs-lookup"><span data-stu-id="545a4-113">OpenGL Functions and Their IRIS GL Equivalents</span></span>](opengl-functions-and-their-iris-gl-equivalents.md)
-   [<span data-ttu-id="545a4-114">Diferenças de íris GL e OpenGL</span><span class="sxs-lookup"><span data-stu-id="545a4-114">IRIS GL and OpenGL Differences</span></span>](iris-gl-and-opengl-differences.md)

 

 




