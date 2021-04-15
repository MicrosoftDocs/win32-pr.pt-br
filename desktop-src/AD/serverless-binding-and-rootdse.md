---
title: Associação sem servidor e RootDSE
description: Se possível, não codifique um nome de servidor.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Associação sem servidor e o AD RootDSE
- AD sem Associação de servidor
- AD RootDSE
- Active Directory, usando, associação, associação sem servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453906"
---
# <a name="serverless-binding-and-rootdse"></a><span data-ttu-id="d5175-107">Associação sem servidor e RootDSE</span><span class="sxs-lookup"><span data-stu-id="d5175-107">Serverless Binding and RootDSE</span></span>

<span data-ttu-id="d5175-108">Se possível, não codifique um nome de servidor.</span><span class="sxs-lookup"><span data-stu-id="d5175-108">If possible, do not hard-code a server name.</span></span> <span data-ttu-id="d5175-109">Além disso, na maioria das circunstâncias, a associação não deve ser desnecessariamente vinculada a um único servidor.</span><span class="sxs-lookup"><span data-stu-id="d5175-109">Furthermore, under most circumstances, binding should not be unnecessarily tied to a single server.</span></span> <span data-ttu-id="d5175-110">Active Directory Domain Services suporte à associação sem servidor, o que significa que Active Directory pode ser associado ao domínio padrão sem especificar o nome de um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="d5175-110">Active Directory Domain Services support serverless binding, which means that Active Directory can be bound to on the default domain without specifying the name of a domain controller.</span></span> <span data-ttu-id="d5175-111">Para aplicativos comuns, normalmente esse é o domínio do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="d5175-111">For ordinary applications, this is typically the domain of the logged-on user.</span></span> <span data-ttu-id="d5175-112">Para aplicativos de serviço, esse é o domínio da conta de logon do serviço ou do cliente que o serviço representa.</span><span class="sxs-lookup"><span data-stu-id="d5175-112">For service applications, this is either the domain of the service logon account or that of the client that the service impersonates.</span></span>

<span data-ttu-id="d5175-113">No LDAP 3,0, o rootDSE é definido como a raiz da árvore de dados do diretório em um servidor de diretório.</span><span class="sxs-lookup"><span data-stu-id="d5175-113">In LDAP 3.0, rootDSE is defined as the root of the directory data tree on a directory server.</span></span> <span data-ttu-id="d5175-114">O rootDSE não faz parte de nenhum namespace.</span><span class="sxs-lookup"><span data-stu-id="d5175-114">The rootDSE is not part of any namespace.</span></span> <span data-ttu-id="d5175-115">A finalidade do rootDSE é fornecer dados sobre o servidor de diretório.</span><span class="sxs-lookup"><span data-stu-id="d5175-115">The purpose of the rootDSE is to provide data about the directory server.</span></span> <span data-ttu-id="d5175-116">A seguir está a cadeia de vinculação usada para associar a rootDSE.</span><span class="sxs-lookup"><span data-stu-id="d5175-116">The following is the binding string that is used to bind to rootDSE.</span></span>


```C++
LDAP://<servername>/rootDSE
```



<span data-ttu-id="d5175-117">O <servername> é o nome DNS de um servidor.</span><span class="sxs-lookup"><span data-stu-id="d5175-117">The <servername> is the DNS name of a server.</span></span> <span data-ttu-id="d5175-118">O <servername> é opcional, conforme mostrado no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5175-118">The <servername> is optional, as shown in the following format.</span></span>


```C++
LDAP://rootDSE
```



<span data-ttu-id="d5175-119">Nesse caso, um controlador de domínio padrão do domínio no qual o contexto de segurança do thread de chamada está será usado.</span><span class="sxs-lookup"><span data-stu-id="d5175-119">In this case, a default domain controller from the domain that the security context of the calling thread is in will be used.</span></span> <span data-ttu-id="d5175-120">Se um controlador de domínio não puder ser acessado no site, o primeiro controlador de domínio que pode ser encontrado será usado.</span><span class="sxs-lookup"><span data-stu-id="d5175-120">If a domain controller cannot be accessed within the site, the first domain controller that can be found will be used.</span></span>

<span data-ttu-id="d5175-121">O rootDSE é um local bem conhecido e confiável em cada servidor de diretório para obter nomes distintos do domínio, do esquema e dos contêineres de configuração, além de outros dados sobre o servidor e o conteúdo de sua árvore de dados de diretório.</span><span class="sxs-lookup"><span data-stu-id="d5175-121">The rootDSE is a well-known and reliable location on every directory server to get distinguished names of the domain, schema, and configuration containers, and other data about the server and the contents of its directory data tree.</span></span> <span data-ttu-id="d5175-122">Essas propriedades raramente mudam em um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="d5175-122">These properties rarely change on a particular server.</span></span> <span data-ttu-id="d5175-123">Um aplicativo pode ler essas propriedades na inicialização e usá-las em toda a sessão.</span><span class="sxs-lookup"><span data-stu-id="d5175-123">An application can read these properties at startup and use them throughout the session.</span></span>

<span data-ttu-id="d5175-124">Em resumo, um aplicativo deve usar a associação sem servidor para associar ao diretório no domínio atual, usar rootDSE para obter o nome distinto de um namespace e usar esse nome distinto para associar a objetos no namespace.</span><span class="sxs-lookup"><span data-stu-id="d5175-124">In summary, an application should use serverless binding to bind to the directory on the current domain, use rootDSE to get the distinguished name for a namespace, and use that distinguished name to bind to objects in the namespace.</span></span>

<span data-ttu-id="d5175-125">Para obter mais informações sobre atributos com suporte do rootDSE, consulte [RootDSE](/windows/desktop/ADSchema/rootdse) na documentação do esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5175-125">For more information about attributes supported by rootDSE, see [RootDSE](/windows/desktop/ADSchema/rootdse) in the Active Directory Schema documentation.</span></span>

<span data-ttu-id="d5175-126">Para obter mais informações e um exemplo de código que mostra como usar a associação sem servidor e o rootDSE, consulte [código de exemplo para obter o nome distinto do domínio](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span><span class="sxs-lookup"><span data-stu-id="d5175-126">For more information and a code example that shows how to use serverless binding and rootDSE, see [Example Code for Getting the Distinguished Name of the Domain](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span></span>

 

 