---
title: Definindo permissões para uma propriedade específica
description: As permissões podem ser definidas para aplicar a uma propriedade específica de um objeto.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Definindo permissões para um anúncio de propriedade específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007287"
---
# <a name="setting-permissions-to-a-specific-property"></a><span data-ttu-id="81c9c-104">Definindo permissões para uma propriedade específica</span><span class="sxs-lookup"><span data-stu-id="81c9c-104">Setting Permissions to a Specific Property</span></span>

<span data-ttu-id="81c9c-105">As permissões podem ser definidas para aplicar a uma propriedade específica de um objeto.</span><span class="sxs-lookup"><span data-stu-id="81c9c-105">Permissions can be set to apply to a specific property of an object.</span></span>

<span data-ttu-id="81c9c-106">**Para definir permissões que se aplicam a uma propriedade específica de um objeto**</span><span class="sxs-lookup"><span data-stu-id="81c9c-106">**To set permissions that apply to a specific property of an object**</span></span>

1.  <span data-ttu-id="81c9c-107">Defina a propriedade [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ Rights \_ DS \_ Read \_ prop** e/ou **ADS \_ Right \_ DS \_ Write \_ prop**.</span><span class="sxs-lookup"><span data-stu-id="81c9c-107">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP** and/or **ADS\_RIGHT\_DS\_WRITE\_PROP**.</span></span>
2.  <span data-ttu-id="81c9c-108">Defina a propriedade [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ de \_ objeto permitido** ou o **\_ objeto ADS AceType \_ acesso \_ negado \_**.</span><span class="sxs-lookup"><span data-stu-id="81c9c-108">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="81c9c-109">Defina a propriedade [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** da propriedade.</span><span class="sxs-lookup"><span data-stu-id="81c9c-109">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the property.</span></span> <span data-ttu-id="81c9c-110">Esse é o **schemaIDGUID** do objeto **attributeSchema** que define a propriedade no esquema.</span><span class="sxs-lookup"><span data-stu-id="81c9c-110">This is the **schemaIDGUID** of the **attributeSchema** object that defines the property in the schema.</span></span> <span data-ttu-id="81c9c-111">O GUID deve ser especificado como uma cadeia de caracteres do formulário produzido pela função [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) na biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="81c9c-111">The GUID must be specified as a string of the form produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function in the COM library.</span></span>
4.  <span data-ttu-id="81c9c-112">Defina [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="81c9c-112">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="81c9c-113">Para obter mais informações sobre o **schemaIDGUID** de um atributo predefinido, consulte [referência de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="81c9c-113">For more information about the **schemaIDGUID** of a predefined attribute, see [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="81c9c-114">Para obter mais informações e um exemplo de código que pode ser usado para recuperar um schemaIDGUID, consulte [lendo objetos attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="81c9c-114">For more information and a code example that can be used to retrieve a schemaIDGUID, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="81c9c-115">Para obter mais informações sobre como criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="81c9c-115">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="81c9c-116">Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE específica de propriedade, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="81c9c-116">For more information and a code example that can be used to set a property-specific ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 