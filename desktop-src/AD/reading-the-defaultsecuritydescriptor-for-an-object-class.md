---
title: Lendo o defaultSecurityDescriptor para uma classe de objeto
description: Usando o ADSI, você pode obter o atributo defaultSecurityDescriptor para uma classe de objeto com a interface IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, lendo o defaultSecurityDescriptor para uma classe de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007296"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="13f90-104">Lendo o defaultSecurityDescriptor para uma classe de objeto</span><span class="sxs-lookup"><span data-stu-id="13f90-104">Reading the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="13f90-105">Usando o ADSI, você pode obter o atributo **defaultSecurityDescriptor** para uma classe de objeto com a interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="13f90-105">Using ADSI, you can obtain the **defaultSecurityDescriptor** attribute for an object class with the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="13f90-106">Para obter o atributo **defaultSecurityDescriptor** para uma classe de objeto, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="13f90-106">To obtain the **defaultSecurityDescriptor** attribute for an object class, perform the following steps.</span></span>

1.  <span data-ttu-id="13f90-107">Obtenha um ponteiro de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) para o objeto **classSchema** da classe Object.</span><span class="sxs-lookup"><span data-stu-id="13f90-107">Get an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface pointer to the **classSchema** object for the object class.</span></span>
2.  <span data-ttu-id="13f90-108">Use o método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para obter o descritor de segurança padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="13f90-108">Use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to get the default security descriptor of the object.</span></span> <span data-ttu-id="13f90-109">O nome da propriedade que contém o descritor de segurança é "defaultSecurityDescriptor".</span><span class="sxs-lookup"><span data-stu-id="13f90-109">The name of the property that contains the security descriptor is "defaultSecurityDescriptor".</span></span> <span data-ttu-id="13f90-110">A propriedade será retornada como uma [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que contém um BSTR com o descritor de segurança padrão no formato de cadeia de caracteres SDDL.</span><span class="sxs-lookup"><span data-stu-id="13f90-110">The property will be returned as a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) containing a BSTR with the default security descriptor in SDDL string format.</span></span>
3.  <span data-ttu-id="13f90-111">Use a função [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para converter o formulário de cadeia de caracteres SDDL em um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="13f90-111">Use the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL string form to a security descriptor.</span></span>
4.  <span data-ttu-id="13f90-112">Use as APIs de segurança [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)e [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) para ler as partes do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="13f90-112">Use the [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner), and [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Security APIs to read the parts of the security descriptor.</span></span>

<span data-ttu-id="13f90-113">Para obter um exemplo de código que demonstra como fazer isso, consulte [exemplo de código para ler defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="13f90-113">For a code example that demonstrates how to do this, see [Example Code for Reading defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span></span>

 

 