---
title: Namespaces
description: Os objetos que residem em um namespace específico são identificados por um nome exclusivo.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- ADSI de namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363649"
---
# <a name="namespaces"></a><span data-ttu-id="aa24b-104">Namespaces</span><span class="sxs-lookup"><span data-stu-id="aa24b-104">Namespaces</span></span>

<span data-ttu-id="aa24b-105">Os objetos que residem em um namespace específico são identificados por um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="aa24b-105">Objects that reside within a given namespace are identified by a unique name.</span></span> <span data-ttu-id="aa24b-106">Por exemplo, os arquivos armazenados em uma unidade de disco do PC residem no namespace do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="aa24b-106">For example, files stored on a PC disk drive reside in the file system namespace.</span></span> <span data-ttu-id="aa24b-107">O nome exclusivo de um arquivo é baseado em onde ele é armazenado no namespace do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="aa24b-107">The unique name of a file is based on where it is stored in the file system namespace.</span></span> <span data-ttu-id="aa24b-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="aa24b-108">For example:</span></span>


```C++
C:\public\documents\adsi\adsi_spec.doc
```



<span data-ttu-id="aa24b-109">Os namespaces do serviço de diretório também identificam os objetos que eles contêm por nomes exclusivos que geralmente são baseados no local no diretório onde o objeto pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="aa24b-109">Directory service namespaces also identify the objects they contain by unique names which are usually based on the location in the directory where the object can be found.</span></span> <span data-ttu-id="aa24b-110">Por exemplo, em um diretório X. 500, um determinado objeto pode ter um nome como este:</span><span class="sxs-lookup"><span data-stu-id="aa24b-110">For example, in an X.500 directory, a given object might have a name like this:</span></span>


```C++
CN=John,OU=Marketing,O=Fabrikam
```



<span data-ttu-id="aa24b-111">Serviços de diretório diferentes usam formulários diferentes para nomear os objetos que eles contêm.</span><span class="sxs-lookup"><span data-stu-id="aa24b-111">Different directory services use different forms for naming the objects they contain.</span></span> <span data-ttu-id="aa24b-112">Isso torna o tratamento de diferentes namespaces desafiador, especialmente para desenvolvedores, considerando todos os diferentes ambientes nos quais o código pode estar em execução.</span><span class="sxs-lookup"><span data-stu-id="aa24b-112">This makes dealing with different namespaces challenging, especially for developers, considering all of the different environments on which the code might be running.</span></span>

<span data-ttu-id="aa24b-113">Uma meta do ADSI (Active Directory Service Interfaces) é fornecer uma estrutura de nomenclatura que permita o acesso a namespaces de diferentes provedores de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="aa24b-113">A goal of Active Directory Service Interfaces (ADSI) is to provide a naming framework that allows access to namespaces of different directory service providers.</span></span>

<span data-ttu-id="aa24b-114">A ADSI define uma Convenção de nomenclatura que pode identificar exclusivamente um objeto em um ambiente heterogêneo.</span><span class="sxs-lookup"><span data-stu-id="aa24b-114">ADSI defines a naming convention that can uniquely identify an object in a heterogeneous environment.</span></span> <span data-ttu-id="aa24b-115">Esses nomes são chamados de cadeias de caracteres ADsPath.</span><span class="sxs-lookup"><span data-stu-id="aa24b-115">These names are called ADsPath strings.</span></span> <span data-ttu-id="aa24b-116">As cadeias de caracteres ADsPath assumem várias formas:</span><span class="sxs-lookup"><span data-stu-id="aa24b-116">ADsPath strings take several forms:</span></span>


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



<span data-ttu-id="aa24b-117">Formatos ADsPath adicionais podem ser introduzidos por diferentes provedores ADSI (como o provedor ADSI para o Serviços de Informações da Internet Server, que dá suporte ao ADsPaths "IIS://").</span><span class="sxs-lookup"><span data-stu-id="aa24b-117">Additional ADsPath formats can be introduced by different ADSI providers (such as the ADSI provider for the Internet Information Services server, which support the "IIS://" ADsPaths).</span></span>

 

 




