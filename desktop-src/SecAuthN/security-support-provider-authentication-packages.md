---
description: O sistema operacional Windows dá suporte à autenticação usando pacotes de segurança que funcionam como ambos os provedores de suporte de segurança e como pacotes de autenticação.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Provedor de suporte de segurança/pacotes de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749891"
---
# <a name="security-support-providerauthentication-packages"></a><span data-ttu-id="a69aa-103">Provedor de suporte de segurança/pacotes de autenticação</span><span class="sxs-lookup"><span data-stu-id="a69aa-103">Security Support Provider/Authentication Packages</span></span>

<span data-ttu-id="a69aa-104">O sistema operacional Windows dá suporte à autenticação usando [*pacotes de segurança*](../secgloss/s-gly.md) que funcionam como ambos os provedores de [*suporte de segurança*](../secgloss/s-gly.md) e como pacotes de [*autenticação*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a69aa-104">The Windows operating system supports authentication using [*security packages*](../secgloss/s-gly.md) that function as both [*security support providers*](../secgloss/s-gly.md) and as [*authentication packages*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="a69aa-105">Os pacotes de segurança fornecem os serviços de suporte do processo de logon de um pacote de autenticação do Windows e também fornecem serviços de autenticação para aplicativos implementando um conjunto de funções que são mapeadas para a SSPI ( [interface do provedor de suporte de segurança](sspi.md) ).</span><span class="sxs-lookup"><span data-stu-id="a69aa-105">Security packages provide the logon process support services of a Windows authentication package and also provide authentication services to applications by implementing a set of functions that are mapped to the [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="a69aa-106">Um pacote de segurança que funciona como um pacote de autenticação e implementa a funcionalidade exigida por [*SSPI*](../secgloss/s-gly.md) é chamado de provedor de suporte de segurança/pacote de autenticação (SSP/AP).</span><span class="sxs-lookup"><span data-stu-id="a69aa-106">A security package that functions as an authentication package and implements the functionality required by [*SSPI*](../secgloss/s-gly.md) is called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="a69aa-107">Para obter mais informações sobre pacotes de segurança, consulte [pacotes SSP fornecidos pela Microsoft](ssp-packages-provided-by-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="a69aa-107">For more information about security packages, see [SSP Packages Provided by Microsoft](ssp-packages-provided-by-microsoft.md).</span></span> <span data-ttu-id="a69aa-108">Para obter informações sobre como desenvolver SSP/APs personalizados, consulte [pacotes de segurança personalizados](custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="a69aa-108">For information about developing custom SSP/APs, see [Custom Security Packages](custom-security-packages.md).</span></span>

 

 
