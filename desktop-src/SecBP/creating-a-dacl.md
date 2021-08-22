---
description: Mostra como criar uma DACL corretamente.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Criando uma DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af1c7c43c24c07d3d301642b93db41496f2ff70742ce8e2e95fd3f7364ad765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516046"
---
# <a name="creating-a-dacl"></a>Criando uma DACL

Criar uma DACL ( [*lista de controle de acesso condicional*](/windows/desktop/SecGloss/d-gly) ) apropriada é uma parte necessária e importante do desenvolvimento de aplicativos. Como uma DACL **nula** permite todos os tipos de acesso a todos os usuários, não use DACLs **nulas** .

O exemplo a seguir mostra como criar corretamente uma DACL. O exemplo contém uma função, CreateMyDACL, que usa a [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) para definir o controle de acesso concedido e negado em uma DACL. Para fornecer acesso diferente para os objetos do seu aplicativo, modifique a função CreateMyDACL conforme necessário.

No exemplo:

1.  A função main passa um endereço de uma estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) para a função CreateMyDACL.
2.  A função CreateMyDACL usa cadeias de caracteres SDDL para:
    -   Negar acesso a usuários convidados e de logon anônimo.
    -   Permitir acesso de leitura/gravação/execução a usuários autenticados.
    -   Permitir controle total para administradores.

    Para obter mais informações sobre os formatos de cadeia de caracteres SDDL, consulte [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  A função CreateMyDACL chama a função [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para converter as cadeias de caracteres SDDL em um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly). O descritor de segurança é apontado pelo membro **lpSecurityDescriptor** da estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . CreateMyDACL envia o valor de retorno de **ConvertStringSecurityDescriptorToSecurityDescriptor** para a função principal.
4.  A função main usa a estrutura [**de \_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) atualizada para especificar a DACL para uma nova pasta que é criada pela função [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .
5.  Quando a função main é concluída usando a estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , a função main libera a memória alocada para o membro **LpSecurityDescriptor** chamando a função [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

> [!Note]  
> Para compilar com êxito funções SDDL, como [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), você deve definir a \_ constante do Win32 \_ WinNT como 0x0500 ou superior.

 


```C++
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <sddl.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

BOOL CreateMyDACL(SECURITY_ATTRIBUTES *);

void main()
{
     SECURITY_ATTRIBUTES  sa;
      
     sa.nLength = sizeof(SECURITY_ATTRIBUTES);
     sa.bInheritHandle = FALSE;  

     // Call function to set the DACL. The DACL
     // is set in the SECURITY_ATTRIBUTES 
     // lpSecurityDescriptor member.
     if (!CreateMyDACL(&sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateMyDACL\n");
         exit(1);
     }

     // Use the updated SECURITY_ATTRIBUTES to specify
     // security attributes for securable objects.
     // This example uses security attributes during
     // creation of a new directory.
     if (0 == CreateDirectory(TEXT("C:\\MyFolder"), &sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateDirectory\n");
         exit(1);
     }

     // Free the memory allocated for the SECURITY_DESCRIPTOR.
     if (NULL != LocalFree(sa.lpSecurityDescriptor))
     {
         // Error encountered; generate message and exit.
         printf("Failed LocalFree\n");
         exit(1);
     }
}


// CreateMyDACL.
//    Create a security descriptor that contains the DACL 
//    you want.
//    This function uses SDDL to make Deny and Allow ACEs.
//
// Parameter:
//    SECURITY_ATTRIBUTES * pSA
//    Pointer to a SECURITY_ATTRIBUTES structure. It is your
//    responsibility to properly initialize the 
//    structure and to free the structure's 
//    lpSecurityDescriptor member when you have
//    finished using it. To free the structure's 
//    lpSecurityDescriptor member, call the 
//    LocalFree function.
// 
// Return value:
//    FALSE if the address to the structure is NULL. 
//    Otherwise, this function returns the value from the
//    ConvertStringSecurityDescriptorToSecurityDescriptor 
//    function.
BOOL CreateMyDACL(SECURITY_ATTRIBUTES * pSA)
{
     // Define the SDDL for the DACL. This example sets 
     // the following access:
     //     Built-in guests are denied all access.
     //     Anonymous logon is denied all access.
     //     Authenticated users are allowed 
     //     read/write/execute access.
     //     Administrators are allowed full control.
     // Modify these values as needed to generate the proper
     // DACL for your application. 
     TCHAR * szSD = TEXT("D:")       // Discretionary ACL
        TEXT("(D;OICI;GA;;;BG)")     // Deny access to 
                                     // built-in guests
        TEXT("(D;OICI;GA;;;AN)")     // Deny access to 
                                     // anonymous logon
        TEXT("(A;OICI;GRGWGX;;;AU)") // Allow 
                                     // read/write/execute 
                                     // to authenticated 
                                     // users
        TEXT("(A;OICI;GA;;;BA)");    // Allow full control 
                                     // to administrators

    if (NULL == pSA)
        return FALSE;

     return ConvertStringSecurityDescriptorToSecurityDescriptor(
                szSD,
                SDDL_REVISION_1,
                &(pSA->lpSecurityDescriptor),
                NULL);
}
```



 

 
