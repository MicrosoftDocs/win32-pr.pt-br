---
description: O provedor base original reportou incorretamente que o algoritmo de hash SHA enumerando algoritmos por chamadas para CryptGetProvParam com o parâmetro PP \_ ENUMALGS especificado.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Funcionalidade de SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646664"
---
# <a name="sha-functionality"></a><span data-ttu-id="2fe15-103">Funcionalidade de SHA</span><span class="sxs-lookup"><span data-stu-id="2fe15-103">SHA Functionality</span></span>

<span data-ttu-id="2fe15-104">O provedor base original reportou incorretamente que o algoritmo de hash [*Sha*](../secgloss/s-gly.md) enumerando algoritmos por chamadas para [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o parâmetro PP \_ ENUMALGS especificado.</span><span class="sxs-lookup"><span data-stu-id="2fe15-104">The original Base Provider incorrectly reported that the [*SHA*](../secgloss/s-gly.md) hash algorithm enumerating algorithms by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with parameter PP\_ENUMALGS specified.</span></span> <span data-ttu-id="2fe15-105">Isso foi corrigido no provedor base.</span><span class="sxs-lookup"><span data-stu-id="2fe15-105">This has been fixed in the Base Provider.</span></span> <span data-ttu-id="2fe15-106">O provedor base revisado e o provedor estendido e agora relatam corretamente o SHA-1.</span><span class="sxs-lookup"><span data-stu-id="2fe15-106">Both the revised Base Provider and the Extended Provider and now correctly report SHA-1.</span></span>

<span data-ttu-id="2fe15-107">Uma constante CALG \_ SHA1 definida foi adicionada a Wincrypt. h com o mesmo valor que CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="2fe15-107">A defined CALG\_SHA1 constant has been added to Wincrypt.h with the same value as CALG\_SHA.</span></span>

 

 
