---
description: Os pacotes de autenticação do Windows fornecem serviços de autenticação implementando a funcionalidade específica do pacote para as funções LsaLogonUser e LsaCallAuthenticationPackage fornecidas pela LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Pacotes de autenticação do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501586"
---
# <a name="windows-authentication-packages"></a><span data-ttu-id="47bd6-103">Pacotes de autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="47bd6-103">Windows Authentication Packages</span></span>

<span data-ttu-id="47bd6-104">Os pacotes de autenticação do Windows fornecem serviços de autenticação implementando a funcionalidade específica do pacote para as funções [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) e [**LSACALLAUTHENTICATIONPACKAGE**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fornecidas pela LSA.</span><span class="sxs-lookup"><span data-stu-id="47bd6-104">Windows authentication packages provide authentication services by implementing package-specific functionality for the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) and [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) functions provided by the LSA.</span></span>

<span data-ttu-id="47bd6-105">MSV1 \_ 0 é um exemplo de um [*pacote de autenticação*](../secgloss/a-gly.md)do Windows.</span><span class="sxs-lookup"><span data-stu-id="47bd6-105">MSV1\_0 is an example of a Windows [*authentication package*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="47bd6-106">O \_ pacote MSV1 0 aceita um nome de usuário e uma senha de [*hash*](../secgloss/h-gly.md) , que é pesquisada no banco de dados Sam (Gerenciador de [*contas de segurança*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="47bd6-106">The MSV1\_0 package accepts a user name and a [*hashed*](../secgloss/h-gly.md) password, which it looks up in the [*Security Accounts Manager*](../secgloss/s-gly.md) (SAM) database.</span></span> <span data-ttu-id="47bd6-107">Dependendo dos resultados da pesquisa, o pacote de autenticação MSV1 \_ 0 aceita ou rejeita a tentativa de autenticação.</span><span class="sxs-lookup"><span data-stu-id="47bd6-107">Depending on the results of the lookup, the MSV1\_0 authentication package accepts or rejects the authentication attempt.</span></span>

<span data-ttu-id="47bd6-108">Para obter uma lista das funções de suporte que o LSA fornece para uso por pacotes de autenticação do Windows que exigem serviços do sistema, consulte [funções de LSA chamadas por pacotes de autenticação](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="47bd6-108">For a list of the support functions the LSA provides for use by Windows authentication packages that require system services, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="47bd6-109">Os pacotes de autenticação do Windows devem implementar um conjunto de funções que são chamadas pelo LSA.</span><span class="sxs-lookup"><span data-stu-id="47bd6-109">Windows authentication packages must implement a set of functions that are called by the LSA.</span></span> <span data-ttu-id="47bd6-110">Para obter a lista completa de funções, consulte [funções implementadas por pacotes de autenticação](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="47bd6-110">For the complete list of functions, see [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

 

 
