---
title: Criando grupos locais
description: Somente grupos locais podem ser criados para servidores membros e para o Windows 2000 Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Criando AD de grupos locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293894"
---
# <a name="creating-local-groups"></a><span data-ttu-id="5d6be-104">Criando grupos locais</span><span class="sxs-lookup"><span data-stu-id="5d6be-104">Creating Local Groups</span></span>

<span data-ttu-id="5d6be-105">Somente grupos locais podem ser criados para servidores membros e para o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5d6be-105">Only local groups can be created for member servers and Windows 2000 Professional.</span></span>

<span data-ttu-id="5d6be-106">**Para criar um grupo local para um servidor membro ou computador que executa o Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="5d6be-106">**To create a local group for a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="5d6be-107">Associe-se ao computador usando as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="5d6be-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="5d6be-108">Use uma conta com direitos suficientes para acessar esse computador.</span><span class="sxs-lookup"><span data-stu-id="5d6be-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="5d6be-109">Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="5d6be-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="5d6be-110">O &lt; parâmetro "nome &gt; do computador" é o nome dos grupos de computadores a serem acessados.</span><span class="sxs-lookup"><span data-stu-id="5d6be-110">The "&lt;computer name&gt;" parameter is the name of the computer groups to access.</span></span>

        <span data-ttu-id="5d6be-111">Na cadeia de caracteres de associação, &lt; o &gt; parâmetro "computador" INSTRUI a ADSI que ela está vinculando a um computador.</span><span class="sxs-lookup"><span data-stu-id="5d6be-111">In the binding string, the "&lt;computer&gt;" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="5d6be-112">A ADSI torna esses dados disponíveis para o analisador do provedor de WinNT para que ele possa ignorar algumas consultas de resolução de ambiguidades para determinar a qual tipo de objeto você está associando.</span><span class="sxs-lookup"><span data-stu-id="5d6be-112">ADSI makes this data available to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="5d6be-113">Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="5d6be-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="5d6be-114">Especifique "local" como a classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para adicionar o grupo.</span><span class="sxs-lookup"><span data-stu-id="5d6be-114">Specify "localGroup" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the group.</span></span>
    > [!Note]  
    > <span data-ttu-id="5d6be-115">Se você especificar "Group" como a classe, a ADSI usará "local".</span><span class="sxs-lookup"><span data-stu-id="5d6be-115">If you specify "group" as the class, ADSI uses "localGroup".</span></span> <span data-ttu-id="5d6be-116">Não especifique a classe como "global".</span><span class="sxs-lookup"><span data-stu-id="5d6be-116">Do not specify the class as "globalGroup".</span></span> <span data-ttu-id="5d6be-117">Os grupos de classe "global Group" não podem ser criados em servidores membros ou em um computador que esteja executando o Windows NT Workstation/Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5d6be-117">Groups of class "globalGroup" cannot be created on member servers or a computer running Windows NT Workstation/Windows 2000 Professional.</span></span> <span data-ttu-id="5d6be-118">Se você especificar "global Group", [**IADsContainer. Create criará**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) o grupo no cache de propriedades, mas [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) não gravará o grupo no banco de dados de segurança e não retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5d6be-118">If you specify "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) creates the group in the property cache, but [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) does not write the group to the security database and it does not return an error.</span></span>

     

3.  <span data-ttu-id="5d6be-119">Grave o grupo no banco de dados de segurança do computador usando [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="5d6be-119">Write the group to the computer security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 