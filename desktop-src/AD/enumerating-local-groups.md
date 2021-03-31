---
title: Enumerando grupos locais
description: Em servidores membros e computadores em execução no Windows 2000 Professional, você pode enumerar todos os grupos locais.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerando grupos locais AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640413"
---
# <a name="enumerating-local-groups"></a><span data-ttu-id="27d0c-104">Enumerando grupos locais</span><span class="sxs-lookup"><span data-stu-id="27d0c-104">Enumerating Local Groups</span></span>

<span data-ttu-id="27d0c-105">Em servidores membros e computadores em execução no Windows 2000 Professional, você pode enumerar todos os grupos locais.</span><span class="sxs-lookup"><span data-stu-id="27d0c-105">On member servers and computers running on Windows 2000 Professional, you can enumerate all local groups.</span></span>

<span data-ttu-id="27d0c-106">Somente grupos locais podem ser criados em servidores membros e no Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="27d0c-106">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="27d0c-107">No entanto, esses grupos locais podem conter:</span><span class="sxs-lookup"><span data-stu-id="27d0c-107">However, those local groups can contain:</span></span>

-   <span data-ttu-id="27d0c-108">Grupos universais e globais da floresta que contém o domínio ao qual o computador é membro.</span><span class="sxs-lookup"><span data-stu-id="27d0c-108">Universal and Global groups from the forest that contains the domain to which the computer is a member.</span></span>
-   <span data-ttu-id="27d0c-109">Grupos locais de domínio do domínio desse computador.</span><span class="sxs-lookup"><span data-stu-id="27d0c-109">Domain local groups from that computer's domain.</span></span>
-   <span data-ttu-id="27d0c-110">Usuários de qualquer domínio na floresta.</span><span class="sxs-lookup"><span data-stu-id="27d0c-110">Users from any domain in the forest.</span></span>

<span data-ttu-id="27d0c-111">**Para enumerar os grupos locais em um servidor membro ou computador que executa o Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="27d0c-111">**To enumerate the local groups on a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="27d0c-112">Associe-se ao computador usando as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="27d0c-112">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="27d0c-113">Use uma conta com direitos suficientes para acessar esse computador.</span><span class="sxs-lookup"><span data-stu-id="27d0c-113">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="27d0c-114">Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="27d0c-114">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="27d0c-115">"O <computer name> parâmetro" é o nome do grupo de computadores a ser acessado.</span><span class="sxs-lookup"><span data-stu-id="27d0c-115">"The <computer name>" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="27d0c-116">Esse parâmetro instrui a ADSI de que está ligando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar a qual tipo de objeto você está ligando.</span><span class="sxs-lookup"><span data-stu-id="27d0c-116">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="27d0c-117">Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="27d0c-117">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="27d0c-118">Defina um filtro que contenha "grupos" usando a propriedade [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="27d0c-118">Set a filter that contains "groups" using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property.</span></span> <span data-ttu-id="27d0c-119">Isso permite que você enumere o contêiner e recupere somente grupos.</span><span class="sxs-lookup"><span data-stu-id="27d0c-119">This enables you to enumerate the container and retrieve only groups.</span></span>
3.  <span data-ttu-id="27d0c-120">Enumere os objetos de grupo, usando o método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="27d0c-120">Enumerate the group objects, using the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method.</span></span>
4.  <span data-ttu-id="27d0c-121">Para cada objeto de grupo, use a interface [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup) para ler o nome e os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="27d0c-121">For each the group object, use the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface to read the name and members of the group.</span></span>

 

 