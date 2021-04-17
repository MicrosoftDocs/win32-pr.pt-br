---
description: LOCALIDADE \_ invariável
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752269"
---
# <a name="locale_invariant"></a><span data-ttu-id="291a7-103">LOCALIDADE \_ invariável</span><span class="sxs-lookup"><span data-stu-id="291a7-103">LOCALE\_INVARIANT</span></span>

<span data-ttu-id="291a7-104">**Windows XP:** A localidade usada para funções de nível de sistema operacional que exigem resultados consistentes e independentes de localidade.</span><span class="sxs-lookup"><span data-stu-id="291a7-104">**Windows XP:** The locale used for operating system-level functions that require consistent and locale-independent results.</span></span> <span data-ttu-id="291a7-105">Por exemplo, a localidade invariável é usada quando um aplicativo compara Cadeias de caracteres usando a função [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e espera um resultado consistente independentemente da localidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="291a7-105">For example, the invariant locale is used when an application compares character strings using the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) function and expects a consistent result regardless of the user locale.</span></span> <span data-ttu-id="291a7-106">As configurações da localidade invariável são semelhantes às do inglês (Estados Unidos), mas não devem ser usadas para exibir dados formatados.</span><span class="sxs-lookup"><span data-stu-id="291a7-106">The settings of the invariant locale are similar to those for English (United States) but should not be used to display formatted data.</span></span> <span data-ttu-id="291a7-107">Normalmente, um aplicativo não usa a localidade \_ invariável porque espera que os resultados de uma ação dependam das regras que regem cada localidade individual.</span><span class="sxs-lookup"><span data-stu-id="291a7-107">Typically, an application does not use LOCALE\_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.</span></span> <span data-ttu-id="291a7-108">O valor de localidade \_ invariável é 0x007F.</span><span class="sxs-lookup"><span data-stu-id="291a7-108">The value of LOCALE\_INVARIANT IS 0x007f.</span></span>

 

 
