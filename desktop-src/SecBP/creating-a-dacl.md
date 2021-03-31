---
description: Mostra como criar uma DACL corretamente.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Criando uma DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf8213f6fbb4e2a885655b47437ec464337ea13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836989"
---
# <a name="creating-a-dacl"></a><span data-ttu-id="f5e41-103">Criando uma DACL</span><span class="sxs-lookup"><span data-stu-id="f5e41-103">Creating a DACL</span></span>

<span data-ttu-id="f5e41-104">Criar uma DACL ( [*lista de controle de acesso condicional*](/windows/desktop/SecGloss/d-gly) ) apropriada é uma parte necessária e importante do desenvolvimento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f5e41-104">Creating a proper [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) is a necessary and important part of application development.</span></span> <span data-ttu-id="f5e41-105">Como uma DACL **nula** permite todos os tipos de acesso a todos os usuários, não use DACLs **nulas** .</span><span class="sxs-lookup"><span data-stu-id="f5e41-105">Because a **NULL** DACL permits all types of access to all users, do not use **NULL** DACLs.</span></span>

<span data-ttu-id="f5e41-106">O exemplo a seguir mostra como criar corretamente uma DACL.</span><span class="sxs-lookup"><span data-stu-id="f5e41-106">The following example shows how to properly create a DACL.</span></span> <span data-ttu-id="f5e41-107">O exemplo contém uma função, CreateMyDACL, que usa a [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) para definir o controle de acesso concedido e negado em uma DACL.</span><span class="sxs-lookup"><span data-stu-id="f5e41-107">The example contains a function, CreateMyDACL, that uses the [security descriptor definition language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) to define the granted and denied access control in a DACL.</span></span> <span data-ttu-id="f5e41-108">Para fornecer acesso diferente para os objetos do seu aplicativo, modifique a função CreateMyDACL conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f5e41-108">To provide different access for your application's objects, modify the CreateMyDACL function as needed.</span></span>

<span data-ttu-id="f5e41-109">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="f5e41-109">In the example:</span></span>

1.  <span data-ttu-id="f5e41-110">A função main passa um endereço de uma estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) para a função CreateMyDACL.</span><span class="sxs-lookup"><span data-stu-id="f5e41-110">The main function passes an address of a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to the CreateMyDACL function.</span></span>
2.  <span data-ttu-id="f5e41-111">A função CreateMyDACL usa cadeias de caracteres SDDL para:</span><span class="sxs-lookup"><span data-stu-id="f5e41-111">The CreateMyDACL function uses SDDL strings to:</span></span>
    -   <span data-ttu-id="f5e41-112">Negar acesso a usuários convidados e de logon anônimo.</span><span class="sxs-lookup"><span data-stu-id="f5e41-112">Deny access to guest and anonymous logon users.</span></span>
    -   <span data-ttu-id="f5e41-113">Permitir acesso de leitura/gravação/execução a usuários autenticados.</span><span class="sxs-lookup"><span data-stu-id="f5e41-113">Allow read/write/execute access to authenticated users.</span></span>
    -   <span data-ttu-id="f5e41-114">Permitir controle total para administradores.</span><span class="sxs-lookup"><span data-stu-id="f5e41-114">Allow full control to administrators.</span></span>

    <span data-ttu-id="f5e41-115">Para obter mais informações sobre os formatos de cadeia de caracteres SDDL, consulte [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="f5e41-115">For more information about the SDDL string formats, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>
3.  <span data-ttu-id="f5e41-116">A função CreateMyDACL chama a função [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para converter as cadeias de caracteres SDDL em um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="f5e41-116">The CreateMyDACL function calls the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL strings to a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="f5e41-117">O descritor de segurança é apontado pelo membro **lpSecurityDescriptor** da estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f5e41-117">The security descriptor is pointed to by the **lpSecurityDescriptor** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="f5e41-118">CreateMyDACL envia o valor de retorno de **ConvertStringSecurityDescriptorToSecurityDescriptor** para a função principal.</span><span class="sxs-lookup"><span data-stu-id="f5e41-118">CreateMyDACL sends the return value from **ConvertStringSecurityDescriptorToSecurityDescriptor** to the main function.</span></span>
4.  <span data-ttu-id="f5e41-119">A função main usa a estrutura [**de \_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) atualizada para especificar a DACL para uma nova pasta que é criada pela função [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="f5e41-119">The main function uses the updated [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to specify the DACL for a new folder that is created by the [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) function.</span></span>
5.  <span data-ttu-id="f5e41-120">Quando a função main é concluída usando a estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , a função main libera a memória alocada para o membro **LpSecurityDescriptor** chamando a função [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="f5e41-120">When the main function is finished using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure, the main function frees the memory allocated for the **lpSecurityDescriptor** member by calling the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="f5e41-121">Para compilar com êxito funções SDDL, como [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), você deve definir a \_ constante do Win32 \_ WinNT como 0x0500 ou superior.</span><span class="sxs-lookup"><span data-stu-id="f5e41-121">To successfully compile SDDL functions such as [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), you must define the \_WIN32\_WINNT constant as 0x0500 or greater.</span></span>

 


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



 

 
