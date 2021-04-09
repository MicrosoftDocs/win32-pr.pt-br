---
description: Ao usar uma interface de aquisição de imagem do Windows (WIA) em mais de um thread em um único processo, um aplicativo deve fornecer marshaling para essa interface.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Usando vários threads em um aplicativo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090491"
---
# <a name="using-multiple-threads-in-a-wia-application"></a><span data-ttu-id="445ba-103">Usando vários threads em um aplicativo WIA</span><span class="sxs-lookup"><span data-stu-id="445ba-103">Using Multiple Threads in a WIA Application</span></span>

<span data-ttu-id="445ba-104">Ao usar uma interface de aquisição de imagem do Windows (WIA) em mais de um thread em um único processo, um aplicativo deve fornecer marshaling para essa interface.</span><span class="sxs-lookup"><span data-stu-id="445ba-104">When using a Windows Image Acquisition (WIA) interface in more than one thread within a single process, an application must provide marshalling for that interface.</span></span> <span data-ttu-id="445ba-105">Se um thread criar um ponteiro de interface, você não poderá usar esse ponteiro em um thread diferente sem Marshalling.</span><span class="sxs-lookup"><span data-stu-id="445ba-105">If one thread creates an interface pointer, you cannot use that pointer in a different thread without marshalling.</span></span>

<span data-ttu-id="445ba-106">Por exemplo, se um thread em um aplicativo obtiver um ponteiro para a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) , um thread separado não poderá usar esse ponteiro de interface sem Marshalling.</span><span class="sxs-lookup"><span data-stu-id="445ba-106">For example, if one thread in an application obtains a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface, a separate thread cannot use that interface pointer without marshalling.</span></span>

<span data-ttu-id="445ba-107">Uma técnica comum usada para realizar esse marshaling é usar a tabela de interface global.</span><span class="sxs-lookup"><span data-stu-id="445ba-107">A common technique used to accomplish this marshalling is to use the global interface table.</span></span> <span data-ttu-id="445ba-108">A tabela de interface global é uma tabela mantida em todos os threads em um único processo.</span><span class="sxs-lookup"><span data-stu-id="445ba-108">The global interface table is a table maintained across all threads within a single process.</span></span> <span data-ttu-id="445ba-109">Todos os threads em execução no processo podem recuperar interfaces registradas para a tabela de interface global.</span><span class="sxs-lookup"><span data-stu-id="445ba-109">All threads running within the process can retrieve interfaces that are registered to the global interface table.</span></span> <span data-ttu-id="445ba-110">Essa técnica evita a necessidade de criar fluxos para passar interfaces entre threads.</span><span class="sxs-lookup"><span data-stu-id="445ba-110">This technique avoids the need to create streams for passing interfaces between threads.</span></span>

<span data-ttu-id="445ba-111">Para obter informações sobre como usar a tabela de interface global, consulte [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="445ba-111">For information on how to use the global interface table, see [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="445ba-112">Mesmo que você não pretenda usar vários threads em um aplicativo WIA, você deve pressupor que todas as funções de transferência de dados ou de retorno de chamada de evento de dispositivo sejam executadas em threads separados.</span><span class="sxs-lookup"><span data-stu-id="445ba-112">Even if you do not intend to use multiple threads in a WIA application, you must assume that all data transfer or device event callback functions run in separate threads.</span></span>

 

 
