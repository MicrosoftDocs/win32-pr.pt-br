---
title: Criando usuários em servidores membros e no Windows 2000 Professional
description: Este tópico descreve as etapas usadas para criar um usuário em um servidor membro ou computador que executa o Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Criando usuários em servidores membros e no AD do Windows 2000 Professional
- AD de usuários, criando um usuário em servidores membros e no Windows 2000 Professional
- Active Directory, usando, usuários, criando um usuário em servidores membros e no Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007336"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="fefb1-106">Criando usuários em servidores membros e no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fefb1-106">Creating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="fefb1-107">**Para criar um usuário**</span><span class="sxs-lookup"><span data-stu-id="fefb1-107">**To create a user**</span></span>

1.  <span data-ttu-id="fefb1-108">Associe-se ao computador usando as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="fefb1-108">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="fefb1-109">Use uma conta que tenha direitos suficientes para acessar esse computador.</span><span class="sxs-lookup"><span data-stu-id="fefb1-109">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="fefb1-110">Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para informar ao ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="fefb1-110">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="fefb1-111">O &lt; computador "nome &gt; do computador" é o nome do computador cujos grupos você deseja acessar.</span><span class="sxs-lookup"><span data-stu-id="fefb1-111">The "&lt;computer name&gt;" computer is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="fefb1-112">Esse parâmetro informa ao ADSI que ele está associando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar o tipo de objeto ao qual você está ligando.</span><span class="sxs-lookup"><span data-stu-id="fefb1-112">This parameter tells ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="fefb1-113">Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="fefb1-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="fefb1-114">Especifique "user" como a classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para adicionar o usuário.</span><span class="sxs-lookup"><span data-stu-id="fefb1-114">Specify "user" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the user.</span></span>
3.  <span data-ttu-id="fefb1-115">Grave o usuário no banco de dados de segurança do computador usando [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="fefb1-115">Write the user to the computer's security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 