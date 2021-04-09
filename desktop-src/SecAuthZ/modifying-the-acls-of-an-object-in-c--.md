---
description: O exemplo a seguir adiciona uma ACE (entrada de controle de acesso) à DACL (lista de controle de acesso discricionário) de um objeto.
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Modificando as ACLs de um objeto em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21195b1164ce949d1305f0c1748d24b0dbb7525b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922517"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a>Modificando as ACLs de um objeto em C++

O exemplo a seguir adiciona uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) à DACL (lista de controle de [*acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) de um objeto.

O parâmetro *AccessMode* determina o tipo de Ace novo e como a nova Ace é combinada com quaisquer ACEs existentes para o Trustee especificado. Use os \_ sinalizadores conceder acesso, definir \_ acesso, negar \_ acesso ou revogar \_ acesso no parâmetro *AccessMode* . Para obter informações sobre esses sinalizadores, [**consulte \_ modo de acesso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Um código semelhante pode ser usado para trabalhar com uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. Especifique \_ \_ as informações de segurança da SACL nas funções [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para obter e definir a SACL do objeto. Use os \_ sinalizadores definir êxito de auditoria \_ , definir \_ falha de auditoria \_ e revogar \_ acesso no parâmetro *AccessMode* . Para obter informações sobre esses sinalizadores, [**consulte \_ modo de acesso**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Use este código para adicionar uma [Ace específica de objeto](object-specific-aces.md) à DACL de um objeto de serviço de diretório. Para especificar os GUIDs em uma ACE específica do objeto, defina o parâmetro *TrusteeForm* como Trustee \_ é \_ Objects \_ e \_ name ou \_ Trustee \_ são objetos \_ e \_ Sid e defina o parâmetro *PszTrustee* como um ponteiro para um [**objeto \_ e um \_ nome**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) ou [**objetos e a estrutura de \_ \_ Sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .

Este exemplo usa a função [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obter a DACL existente. Em seguida, ele preenche uma estrutura de [**\_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) com informações sobre uma ACE e usa a função [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para mesclar a nova ACE com quaisquer ACEs existentes na DACL. Por fim, o exemplo chama a função [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para anexar a nova DACL ao [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) do objeto.


```C++
#include <windows.h>
#include <stdio.h>

DWORD AddAceToObjectsSecurityDescriptor (
    LPTSTR pszObjName,          // name of object
    SE_OBJECT_TYPE ObjectType,  // type of object
    LPTSTR pszTrustee,          // trustee for new ACE
    TRUSTEE_FORM TrusteeForm,   // format of trustee structure
    DWORD dwAccessRights,       // access mask for new ACE
    ACCESS_MODE AccessMode,     // type of ACE
    DWORD dwInheritance         // inheritance flags for new ACE
) 
{
    DWORD dwRes = 0;
    PACL pOldDACL = NULL, pNewDACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea;

    if (NULL == pszObjName) 
        return ERROR_INVALID_PARAMETER;

    // Get a pointer to the existing DACL.

    dwRes = GetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, &pOldDACL, NULL, &pSD);
    if (ERROR_SUCCESS != dwRes) {
        printf( "GetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Initialize an EXPLICIT_ACCESS structure for the new ACE. 

    ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
    ea.grfAccessPermissions = dwAccessRights;
    ea.grfAccessMode = AccessMode;
    ea.grfInheritance= dwInheritance;
    ea.Trustee.TrusteeForm = TrusteeForm;
    ea.Trustee.ptstrName = pszTrustee;

    // Create a new ACL that merges the new ACE
    // into the existing DACL.

    dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetEntriesInAcl Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Attach the new ACL as the object's DACL.

    dwRes = SetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, pNewDACL, NULL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    Cleanup:

        if(pSD != NULL) 
            LocalFree((HLOCAL) pSD); 
        if(pNewDACL != NULL) 
            LocalFree((HLOCAL) pNewDACL); 

        return dwRes;
}

```



 

 
