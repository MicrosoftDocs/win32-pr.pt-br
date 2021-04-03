---
title: Excluindo usuários em servidores membros e no Windows 2000 Professional
description: Este tópico mostra como excluir um usuário de um servidor membro ou computador que executa o Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- usuários AD, excluindo um usuário em servidores membros e Windows 2000 Professional
- Active Directory, usando, usuários, excluindo usuários em servidores membros e Windows 2000 Professional
- excluindo um usuário
- servidor, excluindo um usuário
- excluindo usuários em servidores membros e Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007328"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="aa5f7-108">Excluindo usuários em servidores membros e no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa5f7-108">Deleting Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="aa5f7-109">Este tópico mostra como excluir um usuário de um servidor membro ou computador que executa o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-109">This topic shows how to delete a user from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="aa5f7-110">**Para excluir um usuário**</span><span class="sxs-lookup"><span data-stu-id="aa5f7-110">**To delete a user**</span></span>

1.  <span data-ttu-id="aa5f7-111">Associe-se ao computador usando as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="aa5f7-111">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="aa5f7-112">Use uma conta com direitos suficientes para acessar esse computador.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-112">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="aa5f7-113">Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para informar ao ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="aa5f7-113">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="aa5f7-114">O &lt; parâmetro "nome &gt; do computador" é o nome do computador cujos grupos você deseja acessar.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-114">The "&lt;computer name&gt;" parameter is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="aa5f7-115">Esse parâmetro notifica a ADSI que ele está ligando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar a qual tipo de objeto você está ligando.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-115">This parameter notifies ADSI that it is binding to a computer and allows the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="aa5f7-116">Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="aa5f7-116">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="aa5f7-117">Especifique "user" como a classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) para excluir o usuário.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-117">Specify "user" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) to delete the user.</span></span>

    <span data-ttu-id="aa5f7-118">Lembre-se de que você não precisa chamar [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar a alteração no contêiner.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-118">Be aware that you do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="aa5f7-119">A chamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma a exclusão do usuário diretamente no diretório.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-119">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the user directly to the directory.</span></span>

 

 