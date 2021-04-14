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
# <a name="controlling-child-object-creation-in-c"></a>Controlando a criação de objetos filho em C++

Você pode usar a DACL de um objeto de contêiner para controlar quem tem permissão para criar objetos filho dentro do contêiner. Isso pode ser importante porque o criador de um objeto normalmente é atribuído como o proprietário do objeto, e o proprietário de um objeto pode controlar o acesso ao objeto.

Os vários tipos de objetos de contêiner têm direitos de acesso específicos que controlam a capacidade de criar objetos filho. Por exemplo, um thread deve ter a chave \_ Create \_ sub \_ Key Access para uma chave do registro para criar uma subchave sob a chave. A DACL de uma chave do registro pode conter ACEs que permitem ou negam esse direito de acesso. Da mesma forma, o NTFS dá suporte aos \_ direitos de acesso File Add \_ FILE e File \_ Add \_ de subdiretório para controlar a capacidade de criar arquivos ou diretórios em um diretório.

O direito de acesso de criação filho do AD ADS \_ \_ \_ \_ controla a criação de objetos filho em um objeto de serviço de diretório (DS). No entanto, os objetos DS podem conter diferentes tipos de objetos, portanto, o sistema dá suporte a uma granularidade mais fina do controle. Você pode usar [ACEs específicas de objeto](object-specific-aces.md) para permitir ou negar o direito de criar um tipo especificado de objeto filho. Você pode permitir que um usuário crie um tipo de objeto filho, ao mesmo tempo que impede o usuário de criar outros tipos de objetos filho.

O exemplo a seguir usa a função [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para adicionar uma ACE específica do objeto a uma ACL. A ACE concede permissão para criar um tipo especificado de objeto filho. O membro **grfAccessPermissions** da estrutura [**de \_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) é definido como ADS \_ Right \_ DS \_ Create \_ filho para indicar que a Ace controla a criação do objeto filho. O membro **ObjectsPresent** dos [**objetos e da estrutura \_ \_ Sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) é definido como \_ tipo de objeto ACE \_ \_ presente para indicar que o membro **ObjectTypeGuid** contém um GUID válido. O GUID identifica um tipo de objeto filho cuja criação está sendo controlada.

No exemplo a seguir, pOldDACL deve ser um ponteiro válido para uma estrutura [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) existente. Para obter informações sobre como criar uma estrutura **ACL** para um objeto, consulte [criando um descritor de segurança para um novo objeto em C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).


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



 

 



