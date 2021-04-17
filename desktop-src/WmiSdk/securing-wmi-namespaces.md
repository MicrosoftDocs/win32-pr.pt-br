---
description: O acesso aos namespaces do WMI e seus dados são controlados por descritores de segurança.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Protegendo namespaces WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811718"
---
# <a name="securing-wmi-namespaces"></a><span data-ttu-id="73cab-103">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="73cab-103">Securing WMI Namespaces</span></span>

<span data-ttu-id="73cab-104">O acesso aos namespaces do WMI e seus dados são controlados por [*descritores de segurança*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="73cab-104">Access to WMI namespaces and their data is controlled by [*security descriptors*](gloss-s.md).</span></span> <span data-ttu-id="73cab-105">Você pode proteger dados em seus [*namespaces*](gloss-n.md) ajustando o descritor de segurança do namespace para controlar quem tem acesso aos dados e métodos.</span><span class="sxs-lookup"><span data-stu-id="73cab-105">You can protect data in your [*namespaces*](gloss-n.md) by adjusting the namespace security descriptor to control who has access to the data and methods.</span></span> <span data-ttu-id="73cab-106">Para obter mais informações, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="73cab-106">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>


<span data-ttu-id="73cab-107">Os tópicos a seguir descrevem a segurança do namespace do WMI e como controlar o acesso a namespaces.</span><span class="sxs-lookup"><span data-stu-id="73cab-107">The following topics describe WMI namespace security and how to control access to namespaces.</span></span>

<dl> <dt>

<span data-ttu-id="73cab-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Acesso a namespaces WMI](access-to-wmi-namespaces.md)</span><span class="sxs-lookup"><span data-stu-id="73cab-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Access to WMI Namespaces](access-to-wmi-namespaces.md)</span></span>
</dt> <dd>

<span data-ttu-id="73cab-109">A segurança do namespace do WMI depende de SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) de usuário do Windows e listas de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="73cab-109">WMI namespace security relies on standard Windows user [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) and access control lists.</span></span> <span data-ttu-id="73cab-110">Administradores e usuários têm permissões padrão diferentes.</span><span class="sxs-lookup"><span data-stu-id="73cab-110">Administrators and users have different default permissions.</span></span>

</dd> <dt>

<span data-ttu-id="73cab-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Definindo descritores de segurança de namespace](setting-namespace-security-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="73cab-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)</span></span>
</dt> <dd>

<span data-ttu-id="73cab-112">Depois que um namespace existir no repositório do WMI, você poderá alterar a segurança no namespace usando o controle WMI ou chamando os métodos de [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="73cab-112">After a namespace exists in the WMI repository, you can change the security on the namespace by using the WMI Control or by calling the methods of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="73cab-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="73cab-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="73cab-114">O qualificador **RequiresEncryption** em um namespace requer que o aplicativo cliente WMI ou o script use o nível de autenticação que criptografa chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="73cab-114">The **RequiresEncryption** qualifier on a namespace requires the WMI client application or script to use the authentication level which encrypts remote procedure calls.</span></span> <span data-ttu-id="73cab-115">As solicitações de dados de entrada e os retornos de chamada assíncronos devem ser criptografados.</span><span class="sxs-lookup"><span data-stu-id="73cab-115">Both incoming data requests and asynchronous callbacks must be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="73cab-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Estabelecendo a herança da segurança do namespace](establishing-inheritance-of-namespace-security.md)</span><span class="sxs-lookup"><span data-stu-id="73cab-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establishing Inheritance of Namespace Security](establishing-inheritance-of-namespace-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="73cab-117">Você pode controlar se um namespace filho herda o descritor de segurança do namespace pai.</span><span class="sxs-lookup"><span data-stu-id="73cab-117">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="73cab-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73cab-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73cab-119">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="73cab-119">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="73cab-120">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="73cab-120">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="73cab-121">Criando um namespace com a API do WMI</span><span class="sxs-lookup"><span data-stu-id="73cab-121">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[<span data-ttu-id="73cab-122">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="73cab-122">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
