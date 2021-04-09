---
title: Verificando um direito de acesso de controle na ACL de um objeto
description: Para verificar um direito de acesso de controle na ACL de um objeto, use a função AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Verificando um direito de acesso de controle em um anúncio de ACL de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007355"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a><span data-ttu-id="6a717-104">Verificando um direito de acesso de controle na ACL de um objeto</span><span class="sxs-lookup"><span data-stu-id="6a717-104">Checking a Control Access Right in an Object's ACL</span></span>

<span data-ttu-id="6a717-105">Para verificar um direito de acesso de controle na ACL de um objeto, use a função [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .</span><span class="sxs-lookup"><span data-stu-id="6a717-105">To check a control access right on an object's ACL, use the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span> <span data-ttu-id="6a717-106">Para usar essa função, um aplicativo requer um ponteiro para o [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) do objeto em vez de uma interface [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) para um objeto com descritor de segurança ADSI.</span><span class="sxs-lookup"><span data-stu-id="6a717-106">To use this function, an application requires a pointer to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for the object instead of an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface to an ADSI security descriptor COM object.</span></span>

<span data-ttu-id="6a717-107">Use as seguintes etapas para verificar o acesso de um direito de acesso controlado em um objeto:</span><span class="sxs-lookup"><span data-stu-id="6a717-107">Use the following steps to check access for an controlled access right on an object:</span></span>

1.  <span data-ttu-id="6a717-108">Obtenha um ponteiro de interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) para o objeto.</span><span class="sxs-lookup"><span data-stu-id="6a717-108">Get an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface pointer to the object.</span></span>
2.  <span data-ttu-id="6a717-109">Use o método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para obter o descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="6a717-109">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the security descriptor of the object.</span></span> <span data-ttu-id="6a717-110">O nome da propriedade que contém o descritor de segurança é [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span><span class="sxs-lookup"><span data-stu-id="6a717-110">The name of the property containing the security descriptor is [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span></span> <span data-ttu-id="6a717-111">A propriedade é retornada como um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="6a717-111">The property is returned as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span>
3.  <span data-ttu-id="6a717-112">Use a estrutura do [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) com a função [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para verificar as permissões para o direito de acesso de controle especificado para o cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="6a717-112">Use the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure with the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function to check the permissions for the specified control access right for the specified client.</span></span>

<span data-ttu-id="6a717-113">O código de exemplo no [código de exemplo para a verificação de um direito de acesso de controle na ACL de um objeto](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) mostra, em detalhes, como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6a717-113">The example code in [Example Code for Checking a Control Access Right in an Object's ACL](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) shows, in detail, how to do this.</span></span>

 

 