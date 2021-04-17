---
description: Para melhorar o desempenho, o acesso aos objetos da interface de dispositivo de gráficos (GDI) (como paletas, contextos de dispositivo, regiões e similares) não é serializado.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Vários threads e objetos GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782297"
---
# <a name="multiple-threads-and-gdi-objects"></a><span data-ttu-id="28381-103">Vários threads e objetos GDI</span><span class="sxs-lookup"><span data-stu-id="28381-103">Multiple Threads and GDI Objects</span></span>

<span data-ttu-id="28381-104">Para melhorar o desempenho, o acesso aos objetos da interface de dispositivo de gráficos (GDI) (como paletas, contextos de dispositivo, regiões e similares) não é serializado.</span><span class="sxs-lookup"><span data-stu-id="28381-104">To enhance performance, access to graphics device interface (GDI) objects (such as palettes, device contexts, regions, and the like) is not serialized.</span></span> <span data-ttu-id="28381-105">Isso cria um perigo potencial para processos que têm vários threads compartilhando esses objetos.</span><span class="sxs-lookup"><span data-stu-id="28381-105">This creates a potential danger for processes that have multiple threads sharing these objects.</span></span> <span data-ttu-id="28381-106">Por exemplo, se um thread excluir um objeto GDI enquanto outro thread o estiver usando, os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="28381-106">For example, if one thread deletes a GDI object while another thread is using it, the results are unpredictable.</span></span> <span data-ttu-id="28381-107">Esse perigo pode ser evitado simplesmente por não compartilhar objetos GDI.</span><span class="sxs-lookup"><span data-stu-id="28381-107">This danger can be avoided simply by not sharing GDI objects.</span></span> <span data-ttu-id="28381-108">Se o compartilhamento for inevitável (ou desejável), o aplicativo deverá fornecer seus próprios mecanismos para sincronizar o acesso.</span><span class="sxs-lookup"><span data-stu-id="28381-108">If sharing is unavoidable (or desirable), the application must provide its own mechanisms for synchronizing access.</span></span> <span data-ttu-id="28381-109">Para obter mais informações sobre a sincronização de acesso, consulte [sincronizando a execução de vários threads](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="28381-109">For more information about synchronizing access, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

 

 



