---
title: Definindo direitos para tipos específicos de objetos
description: O procedimento a seguir mostra como definir uma ACE que pode ser herdada somente por uma classe específica de objetos.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- definindo direitos para tipos de objetos AD
- AD de objetos, definindo direitos para
- Active Directory, usando, segurança, definindo direitos para tipos de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917102"
---
# <a name="setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="2af6a-106">Definindo direitos para tipos específicos de objetos</span><span class="sxs-lookup"><span data-stu-id="2af6a-106">Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="2af6a-107">O procedimento a seguir mostra como definir uma ACE que pode ser herdada somente por uma classe específica de objetos.</span><span class="sxs-lookup"><span data-stu-id="2af6a-107">The following procedure shows how to set an ACE that can be inherited only by a specific class of objects.</span></span>

 <span data-ttu-id="2af6a-108">**Para definir uma ACE que pode ser herdada somente por uma classe específica de objetos**</span><span class="sxs-lookup"><span data-stu-id="2af6a-108">**To set an ACE that can be inherited only by a specific class of objects**</span></span>

1.  <span data-ttu-id="2af6a-109">Defina a propriedade [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ de \_ objeto permitido** ou o **\_ objeto ADS AceType \_ acesso \_ negado \_**.</span><span class="sxs-lookup"><span data-stu-id="2af6a-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="2af6a-110">Defina a propriedade [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para incluir o \_ sinalizador de Ace ACEFLAG do ADS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2af6a-110">Set the [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to include the ADS\_ACEFLAG\_INHERIT\_ACE flag.</span></span>
3.  <span data-ttu-id="2af6a-111">Defina a propriedade [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** da classe de objeto que pode herdar a Ace.</span><span class="sxs-lookup"><span data-stu-id="2af6a-111">Set the [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span>
4.  <span data-ttu-id="2af6a-112">Defina a propriedade [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de \_ objeto herdado sinalizador ADS \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="2af6a-112">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_INHERITED OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2af6a-113">Defina **ADS \_ ACEFLAG \_ INHERIT \_ Ace** para fazer com que a Ace seja herdada.</span><span class="sxs-lookup"><span data-stu-id="2af6a-113">Set **ADS\_ACEFLAG\_INHERIT\_ACE** to cause the ACE to be inherited.</span></span> <span data-ttu-id="2af6a-114">Além disso, você deve definir **ADS \_ ACEFLAG \_ herdar \_ somente \_ Ace** se o tipo de objeto ao qual essa Ace se aplica não corresponder ao tipo de objeto do contêiner onde a ACE é especificada.</span><span class="sxs-lookup"><span data-stu-id="2af6a-114">In addition, you must set **ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE** if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="2af6a-115">Se isso não for feito, a ACE também entrará em vigor no contêiner e poderá conceder direitos não pretendidos.</span><span class="sxs-lookup"><span data-stu-id="2af6a-115">If this is not done, the ACE will also become effective on the container and can grant unintended rights.</span></span>

 

<span data-ttu-id="2af6a-116">Para obter mais informações e exemplos de código que podem ser usados para definir esse tipo de ACE, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="2af6a-116">For more information and code examples that can be used to set this type of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 