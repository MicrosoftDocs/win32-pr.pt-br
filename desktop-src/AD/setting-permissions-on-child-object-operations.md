---
title: Definindo permissões em operações de objeto filho
description: As permissões, como criar filho e excluir filho, também podem ser concedidas ou negadas para operações em todos os subobjetos ou subobjetos de uma classe específica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Definindo permissões no AD de operações do objeto filho
- objetos AD, Child, definindo permissões em operações de objeto filho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084433"
---
# <a name="setting-permissions-on-child-object-operations"></a><span data-ttu-id="17838-105">Definindo permissões em operações de objeto filho</span><span class="sxs-lookup"><span data-stu-id="17838-105">Setting Permissions on Child Object Operations</span></span>

<span data-ttu-id="17838-106">As permissões, como criar filho e excluir filho, também podem ser concedidas ou negadas para operações em todos os subobjetos ou subobjetos de uma classe específica.</span><span class="sxs-lookup"><span data-stu-id="17838-106">Permissions, such as Create Child and Delete Child, can also be granted or denied for operations on all subobjects or subobjects of a specific class.</span></span>

<span data-ttu-id="17838-107">O procedimento a seguir pode ser usado para definir permissões para um tipo de subobjeto específico.</span><span class="sxs-lookup"><span data-stu-id="17838-107">The following procedure can be used to set permissions for a specific subobject type.</span></span>

<span data-ttu-id="17838-108">**Para definir permissões para um tipo de subobjeto específico**</span><span class="sxs-lookup"><span data-stu-id="17838-108">**To set permissions for a specific subobject type**</span></span>

1.  <span data-ttu-id="17838-109">Defina a propriedade [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ de \_ objeto permitido** ou o **\_ objeto ADS AceType \_ acesso \_ negado \_**.</span><span class="sxs-lookup"><span data-stu-id="17838-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="17838-110">Defina a propriedade [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o GUID da classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="17838-110">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID for object class.</span></span> <span data-ttu-id="17838-111">Essa é a propriedade **schemaIDGUID** do objeto classSchema que define a classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="17838-111">This is the **schemaIDGUID** property of the classSchema object that defines the object class.</span></span> <span data-ttu-id="17838-112">Se a propriedade **objecttype** for **nula**, a Ace se aplicará a subobjetos de qualquer classe.</span><span class="sxs-lookup"><span data-stu-id="17838-112">If the **ObjectType** property is **NULL**, the ACE applies to subobjects of any class.</span></span>
3.  <span data-ttu-id="17838-113">Defina a propriedade [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="17838-113">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="17838-114">Para obter mais informações e um procedimento para criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="17838-114">For more information and a procedure for creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="17838-115">Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE que controla operações de objeto filho, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="17838-115">For more information and a code example that can be used to set an ACE that controls child object operations, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 