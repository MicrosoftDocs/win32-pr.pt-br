---
title: Detectando o modo de operação de um domínio
description: No Windows 2000, um domínio pode ser executado em dois modos de operação mistos e nativos.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Detectando o modo de operação de um AD de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823666"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a><span data-ttu-id="7b8e4-104">Detectando o modo de operação de um domínio</span><span class="sxs-lookup"><span data-stu-id="7b8e4-104">Detecting the Operation Mode of a Domain</span></span>

<span data-ttu-id="7b8e4-105">No Windows 2000, um domínio pode ser executado em dois modos de operação: misto e nativo.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-105">In Windows 2000, a domain can run in two operation modes: mixed and native.</span></span> <span data-ttu-id="7b8e4-106">O modo misto deve ser usado para incluir controladores de domínio que executam o Windows NT 4,0 em um domínio do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-106">Mixed mode should be used to include domain controllers running Windows NT 4.0 in a Windows 2000 domain.</span></span> <span data-ttu-id="7b8e4-107">O modo misto não dá suporte a grupos universais ou grupos aninhados.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-107">Mixed mode does not support universal groups or nested groups.</span></span> <span data-ttu-id="7b8e4-108">Se todos os controladores de domínio no domínio estiverem executando o Windows 2000, você poderá usar o modo nativo.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-108">If all domain controllers in the domain are running Windows 2000, you can use native mode.</span></span>

<span data-ttu-id="7b8e4-109">Para detectar programaticamente o modo de operação de um domínio do Windows 2000, leia a propriedade [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) do objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) para esse domínio.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-109">To programmatically detect the operation mode of a Windows 2000 domain, read the [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) property of the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object for that domain.</span></span> <span data-ttu-id="7b8e4-110">Um valor de zero (0) significa que o domínio está no modo nativo.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-110">A value of zero (0) means that the domain is in native mode.</span></span> <span data-ttu-id="7b8e4-111">Um valor de um (1) indica que o domínio está no modo misto.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-111">A value of one (1) indicates that the domain is in mixed mode.</span></span> <span data-ttu-id="7b8e4-112">Você também pode usar a função [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) para obter o modo de operação, bem como outros dados sobre o domínio e seu estado.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-112">You can also use the [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) function to get the operation mode as well as other data about the domain and its state.</span></span>

<span data-ttu-id="7b8e4-113">Para associar ao objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) do domínio da conta de usuário sob a qual seu aplicativo está sendo executado, use a associação sem servidor e o RootDSE para obter o nome distinto do domínio e, em seguida, use esse nome distinto para associar ao objeto **domainDns** que representa esse domínio.</span><span class="sxs-lookup"><span data-stu-id="7b8e4-113">To bind to the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object of the domain of the user account under which your application is running, use serverless binding and rootDSE to get the distinguished name for the domain and then use that distinguished name to bind to the **domainDNS** object that represents that domain.</span></span> <span data-ttu-id="7b8e4-114">Para obter mais informações sobre a associação sem servidor e o rootDSE, consulte [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="7b8e4-114">For more information about serverless binding and rootDSE, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="7b8e4-115">Para obter mais informações e um exemplo de código que mostra como detectar programaticamente o modo de operação de um domínio, consulte [código de exemplo para determinar o modo de operação](example-code-for-determining-the-operation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="7b8e4-115">For more information and a code example that shows how to programmatically detect the operation mode of a domain, see [Example Code for Determining the Operation Mode](example-code-for-determining-the-operation-mode.md).</span></span>

 

 