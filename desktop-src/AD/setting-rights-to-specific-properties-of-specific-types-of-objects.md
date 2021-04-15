---
title: Definindo direitos para propriedades específicas de tipos específicos de objetos
description: Permissões específicas de propriedade podem ser usadas em combinação com herança específica de objeto para fornecer a delegação avançada e detalhada de administração.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- definindo direitos para propriedades específicas de tipos específicos de objetos AD
- Active Directory, usando, segurança, definindo direitos para propriedades específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453900"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a><span data-ttu-id="2efd3-105">Definindo direitos para propriedades específicas de tipos específicos de objetos</span><span class="sxs-lookup"><span data-stu-id="2efd3-105">Setting Rights to Specific Properties of Specific Types of Objects</span></span>

<span data-ttu-id="2efd3-106">Permissões específicas de propriedade podem ser usadas em combinação com herança específica de objeto para fornecer a delegação avançada e detalhada de administração.</span><span class="sxs-lookup"><span data-stu-id="2efd3-106">Property-specific permissions can be used in combination with object specific inheritance to provide the powerful and detailed delegation of administration.</span></span> <span data-ttu-id="2efd3-107">Você pode definir uma ACE herdada de objeto específico de propriedade para permitir que um usuário ou grupo especificado Leia e/ou grave um atributo específico em uma classe especificada de objetos filho em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="2efd3-107">You can set a property-specific object-inheritable ACE to allow a specified user or group to read and/or write a specific attribute on a specified class of child objects in a container.</span></span> <span data-ttu-id="2efd3-108">Por exemplo, você pode definir uma ACE em uma UO (unidade organizacional) para habilitar um grupo para ler e gravar o atributo de número de telefone de todos os objetos de usuário na UO.</span><span class="sxs-lookup"><span data-stu-id="2efd3-108">For example, you can set an ACE on an organizational unit (OU) to enable a group to read and write the telephone number attribute of all user objects in the OU.</span></span>

<span data-ttu-id="2efd3-109">**Para definir ACEs herdáveis de objeto específico de propriedade**</span><span class="sxs-lookup"><span data-stu-id="2efd3-109">**To set property-specific object-inheritable ACEs**</span></span>

1.  <span data-ttu-id="2efd3-110">Defina [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ ao \_ objeto permitido** ou ao objeto **ADS \_ AceType \_ acesso \_ negado \_**.</span><span class="sxs-lookup"><span data-stu-id="2efd3-110">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="2efd3-111">Defina [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** do atributo.</span><span class="sxs-lookup"><span data-stu-id="2efd3-111">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the attribute.</span></span> <span data-ttu-id="2efd3-112">Por exemplo, o **schemaIDGUID** do atributo **telephoneNumber** é {bf967a49-0de6-11D0-a285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="2efd3-112">For example, the **schemaIDGUID** of the **telephoneNumber** attribute is {bf967a49-0de6-11d0-a285-00aa003049e2}.</span></span>
3.  <span data-ttu-id="2efd3-113">Defina [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ ACEFLAG \_ INHERIT \_ Ace**.</span><span class="sxs-lookup"><span data-stu-id="2efd3-113">Set [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACEFLAG\_INHERIT\_ACE**.</span></span>
4.  <span data-ttu-id="2efd3-114">Defina [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** da classe de objeto que pode herdar a Ace.</span><span class="sxs-lookup"><span data-stu-id="2efd3-114">Set [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span> <span data-ttu-id="2efd3-115">Por exemplo, o **schemaIDGUID** da classe **User** é {bf967aba-0de6-11D0-a285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="2efd3-115">For example, the **schemaIDGUID** of the **user** class is {bf967aba-0de6-11d0-a285-00aa003049e2}.</span></span>
5.  <span data-ttu-id="2efd3-116">Defina [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente** e o **tipo de \_ \_ objeto herdado sinalizador ADS \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="2efd3-116">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT** and **ADS\_FLAG\_INHERITED\_OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2efd3-117">Defina ADS \_ ACEFLAG \_ INHERIT \_ Ace para fazer com que a Ace seja herdada.</span><span class="sxs-lookup"><span data-stu-id="2efd3-117">Set ADS\_ACEFLAG\_INHERIT\_ACE to cause the ACE to be inherited.</span></span> <span data-ttu-id="2efd3-118">Além disso, Set ADS \_ ACEFLAG \_ herdará \_ somente \_ Ace se o tipo de objeto ao qual essa Ace se aplica não corresponder ao tipo de objeto do contêiner onde a ACE é especificada.</span><span class="sxs-lookup"><span data-stu-id="2efd3-118">In addition, set ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="2efd3-119">Se isso não for feito, a ACE também entrará em vigor no contêiner e poderá conceder direitos inesperados.</span><span class="sxs-lookup"><span data-stu-id="2efd3-119">If this is not done, the ACE will also become effective on the container and can grant unexpected rights.</span></span>

 

<span data-ttu-id="2efd3-120">Para obter mais informações e exemplos de código que podem ser usados para definir esse tipo de ACE, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="2efd3-120">For more information and code examples that can be used to set this kind of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 