---
description: O Windows GDI+ é o subsistema do sistema operacional Windows XP ou do Windows Server 2003 que é responsável por exibir informações sobre telas e impressoras. GDI+ é uma API que é exposta por meio de um conjunto de classes C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Visão geral do GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988860"
---
# <a name="overview-of-gdi"></a><span data-ttu-id="c1a63-104">Visão geral do GDI+</span><span class="sxs-lookup"><span data-stu-id="c1a63-104">Overview of GDI+</span></span>

<span data-ttu-id="c1a63-105">O Windows GDI+ é o subsistema do sistema operacional Windows XP ou do Windows Server 2003 que é responsável por exibir informações sobre telas e impressoras.</span><span class="sxs-lookup"><span data-stu-id="c1a63-105">Windows GDI+ is the subsystem of the Windows XP operating system or Windows Server 2003 that is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="c1a63-106">GDI+ é uma API que é exposta por meio de um conjunto de classes C++.</span><span class="sxs-lookup"><span data-stu-id="c1a63-106">GDI+ is an API that is exposed through a set of C++ classes.</span></span>

<span data-ttu-id="c1a63-107">Como seu nome sugere, o GDI+ é o sucessor do Windows Graphics Device Interface (GDI), a interface gráfica do dispositivo incluída nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="c1a63-107">As its name suggests, GDI+ is the successor to Windows Graphics Device Interface (GDI), the graphics device interface included with earlier versions of Windows.</span></span> <span data-ttu-id="c1a63-108">O Windows XP ou o Windows Server 2003 dá suporte a GDI para compatibilidade com aplicativos existentes, mas os programadores de novos aplicativos devem usar o GDI+ para todas as suas necessidades gráficas, pois a GDI+ otimiza muitos dos recursos do GDI e também fornece recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="c1a63-108">Windows XP or Windows Server 2003 supports GDI for compatibility with existing applications, but programmers of new applications should use GDI+ for all their graphics needs because GDI+ optimizes many of the capabilities of GDI and also provides additional features.</span></span>

<span data-ttu-id="c1a63-109">Uma interface de dispositivo de gráficos, como GDI+, permite que os programadores de aplicativos exibam informações em uma tela ou impressora sem precisar se preocupar com os detalhes de um determinado dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c1a63-109">A graphics device interface, such as GDI+, allows application programmers to display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="c1a63-110">O programador de aplicativos faz chamadas para métodos fornecidos por classes GDI+ e esses métodos, por sua vez, fazem as chamadas apropriadas para drivers de dispositivo específicos.</span><span class="sxs-lookup"><span data-stu-id="c1a63-110">The application programmer makes calls to methods provided by GDI+ classes and those methods in turn make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="c1a63-111">A GDI+ isola o aplicativo do hardware de gráficos e é esse isolamento que permite aos desenvolvedores criar aplicativos independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1a63-111">GDI+ insulates the application from the graphics hardware, and it is this insulation that allows developers to create device-independent applications.</span></span>

 

 



