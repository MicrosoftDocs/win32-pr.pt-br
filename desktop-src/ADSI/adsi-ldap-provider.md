---
title: Provedor LDAP ADSI
description: O provedor de LDAP ADSI implementa um conjunto de objetos ADSI que dão suporte a várias interfaces ADSI. Para acessar o provedor LDAP, associe-se a qualquer um dos objetos LDAP ADSI, usando o ADsPath LDAP.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Provedor LDAP ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822240"
---
# <a name="adsi-ldap-provider"></a><span data-ttu-id="35adb-105">Provedor LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="35adb-105">ADSI LDAP Provider</span></span>

<span data-ttu-id="35adb-106">O provedor de LDAP ADSI implementa um conjunto de objetos ADSI que dão suporte a várias interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="35adb-106">The ADSI LDAP Provider implements a set of ADSI objects that support various ADSI interfaces.</span></span> <span data-ttu-id="35adb-107">Para acessar o provedor LDAP, associe-se a qualquer um dos objetos LDAP ADSI, usando o ADsPath LDAP.</span><span class="sxs-lookup"><span data-stu-id="35adb-107">To access the LDAP provider, bind to any of the ADSI LDAP objects, using the LDAP ADsPath.</span></span>

<span data-ttu-id="35adb-108">Você deve ter Adsldp.dll, Adsldpc.dll, Adsmsext.dll e Activeds.dll instalados no computador cliente para trabalhar com o provedor.</span><span class="sxs-lookup"><span data-stu-id="35adb-108">You must have Adsldp.dll, Adsldpc.dll, Adsmsext.dll, and Activeds.dll installed on your client computer to work with the provider.</span></span>

> [!Note]  
> <span data-ttu-id="35adb-109">O provedor LDAP ADSI padrão não pode ser considerado totalmente seguro para thread.</span><span class="sxs-lookup"><span data-stu-id="35adb-109">The default ADSI LDAP provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="35adb-110">Os gravadores de aplicativos multissegmentados devem coordenar corretamente o acesso entre os threads por meio do uso adequado de objetos de sincronização, como semáforos, exclusões mútuas, seções críticas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="35adb-110">Writers of multithreaded applications should properly coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




