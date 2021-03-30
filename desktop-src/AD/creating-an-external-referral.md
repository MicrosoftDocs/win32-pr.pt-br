---
title: Criando uma referência externa
description: Se um objeto crossRef externo for criado e um controlador de domínio o usar para gerar uma referência, o objeto crossRef fornecerá dois elementos de dados importantes nas propriedades a seguir.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- Active Directory de referências externas
- Exemplos de Active Directory Active Directory, criando uma referência externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640422"
---
# <a name="creating-an-external-referral"></a><span data-ttu-id="3b588-105">Criando uma referência externa</span><span class="sxs-lookup"><span data-stu-id="3b588-105">Creating an External Referral</span></span>

<span data-ttu-id="3b588-106">Se um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) externo for criado e um controlador de domínio o usar para gerar uma referência, o objeto **crossRef** fornecerá dois elementos de dados importantes nas propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b588-106">If an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is created and a domain controller uses it to generate a referral, the **crossRef** object provides two important data elements in the following properties.</span></span> <span data-ttu-id="3b588-107">Para obter mais informações sobre situações em que isso pode ocorrer, consulte a seção anterior.</span><span class="sxs-lookup"><span data-stu-id="3b588-107">For more information about situations where this can occur, see the previous section.</span></span>



| <span data-ttu-id="3b588-108">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3b588-108">Property</span></span>                           | <span data-ttu-id="3b588-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b588-109">Description</span></span>                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b588-110">**dnsRoot**</span><span class="sxs-lookup"><span data-stu-id="3b588-110">**dnsRoot**</span></span>](/windows/desktop/ADSchema/a-dnsroot) | <span data-ttu-id="3b588-111">Especifica o servidor ou domínio que pode fornecer dados do contexto de nomenclatura especificado no [**NCName**](/windows/desktop/ADSchema/a-ncname).</span><span class="sxs-lookup"><span data-stu-id="3b588-111">Specifies the server or domain that can serve data from the naming context specified in [**nCName**](/windows/desktop/ADSchema/a-ncname).</span></span>                                           |
| [<span data-ttu-id="3b588-112">**nCName**</span><span class="sxs-lookup"><span data-stu-id="3b588-112">**nCName**</span></span>](/windows/desktop/ADSchema/a-ncname)   | <span data-ttu-id="3b588-113">Especifica o nome distinto para o domínio, esquema ou contêiner de configuração com raiz no servidor ou domínio especificado por [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot).</span><span class="sxs-lookup"><span data-stu-id="3b588-113">Specifies the distinguished name for the domain, schema, or configuration container rooted at the server or domain specified by [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span></span> |



 

<span data-ttu-id="3b588-114">Por exemplo, se o servidor com o endereço DNS de serv1.northwest.Fabrikam.com fornece o contexto de nomenclatura com raiz em CN = MyContainer, OU = MyDOM, O = Fabrikam, defina o [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot) como o endereço DNS desse servidor e o [**NCName**](/windows/desktop/ADSchema/a-ncname) como o nome distinto do contêiner de domínio, esquema ou configuração.</span><span class="sxs-lookup"><span data-stu-id="3b588-114">For example, if the server with DNS address of serv1.northwest.Fabrikam.com serves the naming context rooted at CN=MyContainer,OU=MyDOM,O=Fabrikam, set the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) to that server's DNS address and the [**nCName**](/windows/desktop/ADSchema/a-ncname) to the distinguished name of the domain, schema, or configuration container.</span></span>

<span data-ttu-id="3b588-115">Para obter mais informações e um exemplo de código que mostra como criar uma referência externa, consulte [exemplo de código para criar um objeto crossRef externo](example-code-for-creating-an-external-crossref-object.md).</span><span class="sxs-lookup"><span data-stu-id="3b588-115">For more information and a code example that shows how to create an external referral, see [Example Code for Creating an External crossRef Object](example-code-for-creating-an-external-crossref-object.md).</span></span>

 

 