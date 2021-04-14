---
description: Você pode usar a DACL de um objeto de contêiner para controlar quem tem permissão para criar objetos filho dentro do contêiner.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Controlando a criação de objetos filho em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502184"
---
# <a name="controlling-child-object-creation-in-c"></a><span data-ttu-id="525e4-103">Controlando a criação de objetos filho em C++</span><span class="sxs-lookup"><span data-stu-id="525e4-103">Controlling Child Object Creation in C++</span></span>

<span data-ttu-id="525e4-104">Você pode usar a DACL de um objeto de contêiner para controlar quem tem permissão para criar objetos filho dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="525e4-104">You can use the DACL of a container object to control who is allowed to create child objects within the container.</span></span> <span data-ttu-id="525e4-105">Isso pode ser importante porque o criador de um objeto normalmente é atribuído como o proprietário do objeto, e o proprietário de um objeto pode controlar o acesso ao objeto.</span><span class="sxs-lookup"><span data-stu-id="525e4-105">This can be important because the creator of an object is typically assigned as the object's owner, and an object's owner can control access to the object.</span></span>

<span data-ttu-id="525e4-106">Os vários tipos de objetos de contêiner têm direitos de acesso específicos que controlam a capacidade de criar objetos filho.</span><span class="sxs-lookup"><span data-stu-id="525e4-106">The various types of container objects have specific access rights that control the ability to create child objects.</span></span> <span data-ttu-id="525e4-107">Por exemplo, um thread deve ter a chave \_ Create \_ sub \_ Key Access para uma chave do registro para criar uma subchave sob a chave.</span><span class="sxs-lookup"><span data-stu-id="525e4-107">For example, a thread must have KEY\_CREATE\_SUB\_KEY access to a registry key to create a subkey under the key.</span></span> <span data-ttu-id="525e4-108">A DACL de uma chave do registro pode conter ACEs que permitem ou negam esse direito de acesso.</span><span class="sxs-lookup"><span data-stu-id="525e4-108">The DACL of a registry key can contain ACEs that allow or deny this access right.</span></span> <span data-ttu-id="525e4-109">Da mesma forma, o NTFS dá suporte aos \_ direitos de acesso File Add \_ FILE e File \_ Add \_ de subdiretório para controlar a capacidade de criar arquivos ou diretórios em um diretório.</span><span class="sxs-lookup"><span data-stu-id="525e4-109">Similarly, NTFS supports the FILE\_ADD\_FILE and FILE\_ADD\_SUBDIRECTORY access rights for controlling the ability to create files or directories in a directory.</span></span>

<span data-ttu-id="525e4-110">O direito de acesso de criação filho do AD ADS \_ \_ \_ \_ controla a criação de objetos filho em um objeto de serviço de diretório (DS).</span><span class="sxs-lookup"><span data-stu-id="525e4-110">The ADS\_RIGHT\_DS\_CREATE\_CHILD access right controls the creation of child objects in a directory service (DS) object.</span></span> <span data-ttu-id="525e4-111">No entanto, os objetos DS podem conter diferentes tipos de objetos, portanto, o sistema dá suporte a uma granularidade mais fina do controle.</span><span class="sxs-lookup"><span data-stu-id="525e4-111">However, DS objects can contain different types of objects, so the system supports a finer granularity of control.</span></span> <span data-ttu-id="525e4-112">Você pode usar [ACEs específicas de objeto](object-specific-aces.md) para permitir ou negar o direito de criar um tipo especificado de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="525e4-112">You can use [object-specific ACEs](object-specific-aces.md) to allow or deny the right to create a specified type of child object.</span></span> <span data-ttu-id="525e4-113">Você pode permitir que um usuário crie um tipo de objeto filho, ao mesmo tempo que impede o usuário de criar outros tipos de objetos filho.</span><span class="sxs-lookup"><span data-stu-id="525e4-113">You can allow a user to create one type of child object while preventing the user from creating other types of child objects.</span></span>

<span data-ttu-id="525e4-114">O exemplo a seguir usa a função [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para adicionar uma ACE específica do objeto a uma ACL.</span><span class="sxs-lookup"><span data-stu-id="525e4-114">The following example uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to add an object-specific ACE to an ACL.</span></span> <span data-ttu-id="525e4-115">A ACE concede permissão para criar um tipo especificado de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="525e4-115">The ACE grants permission to create a specified type of child object.</span></span> <span data-ttu-id="525e4-116">O membro **grfAccessPermissions** da estrutura [**de \_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) é definido como ADS \_ Right \_ DS \_ Create \_ filho para indicar que a Ace controla a criação do objeto filho.</span><span class="sxs-lookup"><span data-stu-id="525e4-116">The **grfAccessPermissions** member of the [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure is set to ADS\_RIGHT\_DS\_CREATE\_CHILD to indicate that the ACE controls the child object creation.</span></span> <span data-ttu-id="525e4-117">O membro **ObjectsPresent** dos [**objetos e da estrutura \_ \_ Sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) é definido como \_ tipo de objeto ACE \_ \_ presente para indicar que o membro **ObjectTypeGuid** contém um GUID válido.</span><span class="sxs-lookup"><span data-stu-id="525e4-117">The **ObjectsPresent** member of the [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure is set to ACE\_OBJECT\_TYPE\_PRESENT to indicate that the **ObjectTypeGuid** member contains a valid GUID.</span></span> <span data-ttu-id="525e4-118">O GUID identifica um tipo de objeto filho cuja criação está sendo controlada.</span><span class="sxs-lookup"><span data-stu-id="525e4-118">The GUID identifies a type of child object whose creation is being controlled.</span></span>

<span data-ttu-id="525e4-119">No exemplo a seguir, pOldDACL deve ser um ponteiro válido para uma estrutura [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) existente.</span><span class="sxs-lookup"><span data-stu-id="525e4-119">In the following example, pOldDACL must be a valid pointer to an existing [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) structure.</span></span> <span data-ttu-id="525e4-120">Para obter informações sobre como criar uma estrutura **ACL** para um objeto, consulte [criando um descritor de segurança para um novo objeto em C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="525e4-120">For information about how to create an **ACL** structure for an object, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 



