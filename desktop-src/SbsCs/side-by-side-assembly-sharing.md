---
description: A figura a seguir ilustra como dois aplicativos podem compartilhar um assembly usando o método tradicional de compartilhamento de assembly.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Compartilhamento de assembly lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922532"
---
# <a name="side-by-side-assembly-sharing"></a><span data-ttu-id="fadd7-103">Compartilhamento de assembly lado a lado</span><span class="sxs-lookup"><span data-stu-id="fadd7-103">Side-by-side Assembly Sharing</span></span>

<span data-ttu-id="fadd7-104">A figura a seguir ilustra como dois aplicativos podem compartilhar um assembly usando o método tradicional de compartilhamento de assembly.</span><span class="sxs-lookup"><span data-stu-id="fadd7-104">The following figure illustrates how two applications might share an assembly using the traditional method of assembly sharing.</span></span> <span data-ttu-id="fadd7-105">Um problema com o compartilhamento de assembly tradicional ocorre quando um aplicativo instala uma versão de um assembly, normalmente uma DLL, que não é compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="fadd7-105">A problem with traditional assembly sharing occurs when an application installs a version of an assembly—commonly a DLL—that is not backward compatible.</span></span> <span data-ttu-id="fadd7-106">O aplicativo acabou de instalar funciona, mas os aplicativos que dependem da versão anterior da DLL podem não funcionar mais.</span><span class="sxs-lookup"><span data-stu-id="fadd7-106">The application just installed works, but applications that depended on the previous DLL version may no longer work.</span></span>

![representação de dois aplicativos que compartilham um assembly](images/sxs1.png)

<span data-ttu-id="fadd7-108">O aplicativo isolado e a solução de assembly lado a lado permitem que versões diferentes do mesmo assembly Win32 sejam executadas ao mesmo tempo no mesmo sistema sem conflito.</span><span class="sxs-lookup"><span data-stu-id="fadd7-108">The isolated application and side-by-side assembly solution enables different versions of the same Win32 assembly to run at the same time on the same system without conflict.</span></span> <span data-ttu-id="fadd7-109">Ao especificar qual versão do assembly lado a lado o aplicativo deve usar, os desenvolvedores podem garantir que a configuração testada sempre será duplicada no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="fadd7-109">By specifying which side-by-side assembly version the application should use, developers can guarantee that the configuration they test will always be duplicated on the user's computer.</span></span> <span data-ttu-id="fadd7-110">O compartilhamento lado a lado é ilustrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="fadd7-110">Side-by-side sharing is illustrated in the following figure.</span></span>

![implementação de compartilhamento de assembly lado a lado](images/sxs2.png)

<span data-ttu-id="fadd7-112">Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="fadd7-112">For more information, see [About Isolated Applications and Side-by-side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

 

 



