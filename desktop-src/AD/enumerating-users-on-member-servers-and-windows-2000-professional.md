---
title: Enumerando usuários em servidores membros e no Windows 2000 Professional
description: Este tópico mostra como enumerar todos os usuários, em um banco de dados de segurança local, em servidores membros e computadores em execução no Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Enumerando usuários em servidores membros e Windows 2000 Professional AD
- AD de usuários, enumerando usuários em servidores membros e Windows 2000 Professional
- Active Directory, usando, usuários, enumerando usuários em servidores membros e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640412"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="3e762-106">Enumerando usuários em servidores membros e no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e762-106">Enumerating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="3e762-107">Este tópico mostra como enumerar todos os usuários, em um banco de dados de segurança local, em servidores membros e computadores em execução no Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3e762-107">This topic shows how to enumerate all users, in a local security database, on member servers and computers running on Windows 2000 Professional.</span></span>

<span data-ttu-id="3e762-108">**Para enumerar os usuários**</span><span class="sxs-lookup"><span data-stu-id="3e762-108">**To enumerate the users**</span></span>

1.  <span data-ttu-id="3e762-109">Associe-se ao computador usando as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="3e762-109">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="3e762-110">Use uma conta que tenha direitos suficientes para acessar esse computador.</span><span class="sxs-lookup"><span data-stu-id="3e762-110">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="3e762-111">Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="3e762-111">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="3e762-112">O &lt; parâmetro "nome &gt; do computador" é o nome do computador para cujos grupos serão acessados.</span><span class="sxs-lookup"><span data-stu-id="3e762-112">The "&lt;computer name&gt;" parameter is the name of the computer for whose groups to access.</span></span> <span data-ttu-id="3e762-113">Esse parâmetro instrui a ADSI de que ela está vinculando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar o tipo de objeto ao qual você está ligando.</span><span class="sxs-lookup"><span data-stu-id="3e762-113">This parameter instructs ADSI that it is binding to a computer and enables the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="3e762-114">Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="3e762-114">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="3e762-115">Adicione "user" à propriedade [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="3e762-115">Add "user" to the [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) property.</span></span> <span data-ttu-id="3e762-116">Isso faz com que a enumeração contenha apenas objetos que tenham a classe de objeto "user".</span><span class="sxs-lookup"><span data-stu-id="3e762-116">This causes the enumeration to only contain objects that have the "user" object class.</span></span>
3.  <span data-ttu-id="3e762-117">Enumere os objetos.</span><span class="sxs-lookup"><span data-stu-id="3e762-117">Enumerate the objects.</span></span> <span data-ttu-id="3e762-118">Para cada objeto de usuário, use os métodos de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) para ler as propriedades do usuário.</span><span class="sxs-lookup"><span data-stu-id="3e762-118">For each user object, use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) interface methods to read the user properties.</span></span>

 

 