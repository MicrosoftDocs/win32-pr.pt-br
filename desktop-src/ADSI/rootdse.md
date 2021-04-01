---
title: RootDSE (ADSI)
description: Cada servidor de diretório tem uma entrada exclusiva chamada RootDSE. Ele fornece dados sobre o servidor, como seus recursos, a versão LDAP à qual ele dá suporte e os contextos de nomenclatura que ele usa.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641835"
---
# <a name="rootdse-adsi"></a><span data-ttu-id="6a629-104">RootDSE (ADSI)</span><span class="sxs-lookup"><span data-stu-id="6a629-104">RootDSE (ADSI)</span></span>

<span data-ttu-id="6a629-105">Cada servidor de diretório tem uma entrada exclusiva chamada **RootDSE**.</span><span class="sxs-lookup"><span data-stu-id="6a629-105">Each directory server has a unique entry called **RootDSE**.</span></span> <span data-ttu-id="6a629-106">Ele fornece dados sobre o servidor, como seus recursos, a versão LDAP à qual ele dá suporte e os contextos de nomenclatura que ele usa.</span><span class="sxs-lookup"><span data-stu-id="6a629-106">It provides data about the server, such as its capabilities, the LDAP version it supports, and the naming contexts it uses.</span></span>

<span data-ttu-id="6a629-107">Por exemplo, para criar um script, ou aplicativo, que possa ser executado em qualquer ambiente de domínio do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a629-107">For example, to create a script, or application, that can run on any Windows domain environment.</span></span> <span data-ttu-id="6a629-108">Você pode especificar o nome distinto, o nome do servidor ou o nome de domínio ao se conectar a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a629-108">You can specify either the distinguished name, server name, or domain name when connecting to Active Directory.</span></span> <span data-ttu-id="6a629-109">Se você não tiver essas informações, poderá usar o objeto **RootDSE** para estabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="6a629-109">If you do not have this information, you can then use the **RootDSE** object to establish a connection.</span></span> <span data-ttu-id="6a629-110">O exemplo de código a seguir altera a descrição de domínio em qualquer domínio.</span><span class="sxs-lookup"><span data-stu-id="6a629-110">The following code example changes the domain description in any domain.</span></span>


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



<span data-ttu-id="6a629-111">Ao obter o atributo **defaultNamingContext** de **RootDSE**, você pode associar ao domínio atual, por exemplo, a Fabrikam **defaultNamingContext** é DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="6a629-111">By getting the **defaultNamingContext** attribute from **RootDSE**, you can bind to the current domain, for example, the Fabrikam **defaultNamingContext** is DC=Fabrikam, DC=COM.</span></span>

<span data-ttu-id="6a629-112">Para enumerar as propriedades do **RootDSE**, use a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) .</span><span class="sxs-lookup"><span data-stu-id="6a629-112">To enumerate the properties of the **RootDSE**, use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface.</span></span> <span data-ttu-id="6a629-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) não pode ser usado para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="6a629-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) cannot be used for this task.</span></span>

<span data-ttu-id="6a629-114">Para obter mais informações, consulte [associação sem servidor e RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span><span class="sxs-lookup"><span data-stu-id="6a629-114">For more information, see [Serverless Binding and RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span></span>

 

 