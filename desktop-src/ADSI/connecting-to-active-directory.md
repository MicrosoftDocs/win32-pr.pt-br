---
title: Conectando-se ao Active Directory
description: Há vários métodos usados para acessar Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Conectando-se ao Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915909"
---
# <a name="connecting-to-active-directory"></a><span data-ttu-id="2a466-104">Conectando-se ao Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a466-104">Connecting to Active Directory</span></span>

<span data-ttu-id="2a466-105">Há vários métodos usados para acessar Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a466-105">There are several methods used to access Active Directory.</span></span> <span data-ttu-id="2a466-106">É recomendável que você use a API ADSI para acessar Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a466-106">It is recommended that you use the ADSI API to access Active Directory.</span></span> <span data-ttu-id="2a466-107">A ADSI implementa o protocolo LDAP para se comunicar com Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a466-107">ADSI implements the LDAP protocol to communicate with Active Directory.</span></span> <span data-ttu-id="2a466-108">Os exemplos de código a seguir mostram como acessar Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a466-108">The following code examples show how to access Active Directory.</span></span>


```VB
Set ns = GetObject("LDAP:")
```



<span data-ttu-id="2a466-109">Isso abre o provedor LDAP e o prepara para recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="2a466-109">This opens the LDAP provider and prepares it to retrieve data.</span></span> <span data-ttu-id="2a466-110">Nenhuma conexão é estabelecida até que os dados sejam solicitados.</span><span class="sxs-lookup"><span data-stu-id="2a466-110">No connection is established until data is requested.</span></span> <span data-ttu-id="2a466-111">Quando os dados são solicitados, o ADSI, com a ajuda do serviço localizador, tenta encontrar o melhor DC (controlador de domínio) para a conexão e estabelecerá uma conexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="2a466-111">When data is requested, ADSI, with the help of the locator service, attempts to find the best domain controller (DC) for the connection and will establish a connection to the server.</span></span> <span data-ttu-id="2a466-112">Esse processo é conhecido como associação sem servidor.</span><span class="sxs-lookup"><span data-stu-id="2a466-112">This process is known as serverless binding.</span></span>

<span data-ttu-id="2a466-113">A ADSI também permite que você especifique o nome do servidor a ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="2a466-113">ADSI also enables you to specify the server name to use for the connection.</span></span>


```VB
Set obj = GetObject("LDAP://mysrv01")
```



<span data-ttu-id="2a466-114">Em outro cenário, você só pode saber o nome de domínio, mas não o nome do servidor específico.</span><span class="sxs-lookup"><span data-stu-id="2a466-114">In another scenario, you may only know the domain name but not the specific server name.</span></span> <span data-ttu-id="2a466-115">Novamente, a ADSI permite que você especifique o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="2a466-115">Again, ADSI enables you to specify the domain name.</span></span> <span data-ttu-id="2a466-116">No Windows 2000, o nome de domínio é representado como um nome DNS.</span><span class="sxs-lookup"><span data-stu-id="2a466-116">In Windows 2000, the domain name is represented as a DNS name.</span></span> <span data-ttu-id="2a466-117">Por exemplo, se Joe Worden, o administrador de rede, optar por se conectar usando o nome de domínio, ele poderá usar o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a466-117">For example, if Joe Worden, the network administrator, chooses to connect using the domain name, he could use the following code example.</span></span>


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



<span data-ttu-id="2a466-118">A ADSI se conectará a um dos controladores de domínio no domínio fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="2a466-118">ADSI will connect to one of the domain controllers in the fabrikam.com domain.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a466-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a466-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a466-120">Associação a objetos Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a466-120">Binding to Active Directory Objects</span></span>](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




