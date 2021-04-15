---
title: Excluindo grupos locais
description: Este tópico mostra como excluir um grupo local de um servidor membro ou computador que executa o Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Excluindo grupos locais AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453936"
---
# <a name="deleting-local-groups"></a><span data-ttu-id="56b18-104">Excluindo grupos locais</span><span class="sxs-lookup"><span data-stu-id="56b18-104">Deleting Local Groups</span></span>

<span data-ttu-id="56b18-105">Este tópico mostra como excluir um grupo local de um servidor membro ou computador que executa o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="56b18-105">This topic shows how to delete a local group from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="56b18-106">**Para excluir um grupo local**</span><span class="sxs-lookup"><span data-stu-id="56b18-106">**To delete a local group**</span></span>

1.  <span data-ttu-id="56b18-107">Associe-se ao computador usando as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="56b18-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="56b18-108">Use uma conta com direitos suficientes para acessar esse computador.</span><span class="sxs-lookup"><span data-stu-id="56b18-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="56b18-109">Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="56b18-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="56b18-110">O &lt; parâmetro "nome &gt; do computador" é o nome do grupo de computadores a ser acessado.</span><span class="sxs-lookup"><span data-stu-id="56b18-110">The "&lt;computer name&gt;" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="56b18-111">Esse parâmetro instrui a ADSI de que está ligando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar a qual tipo de objeto você está ligando.</span><span class="sxs-lookup"><span data-stu-id="56b18-111">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="56b18-112">Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="56b18-112">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="56b18-113">Especifique "Group" como a classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)para excluir o grupo.</span><span class="sxs-lookup"><span data-stu-id="56b18-113">Specify "group" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)to delete the group.</span></span>

    <span data-ttu-id="56b18-114">Você não precisa chamar [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar a alteração no contêiner.</span><span class="sxs-lookup"><span data-stu-id="56b18-114">You do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="56b18-115">A chamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma a exclusão do grupo diretamente para o diretório.</span><span class="sxs-lookup"><span data-stu-id="56b18-115">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the group directly to the directory.</span></span>

 

 