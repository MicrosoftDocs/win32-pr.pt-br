---
description: Um programa de controle de serviço pode criar ou modificar a DACL associada a um serviço para controlar o acesso.
ms.assetid: 24bfb2b5-34be-4d38-a690-90d29f5d4f9c
title: Modificando a DACL de um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d814f6bc81b6d6a207bebf0e9b88c0bb672cdfbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829634"
---
# <a name="modifying-the-dacl-for-a-service"></a><span data-ttu-id="a4c33-103">Modificando a DACL de um serviço</span><span class="sxs-lookup"><span data-stu-id="a4c33-103">Modifying the DACL for a Service</span></span>

<span data-ttu-id="a4c33-104">Um [programa de controle de serviço](service-control-programs.md) pode criar ou modificar a DACL associada a um serviço para controlar o acesso.</span><span class="sxs-lookup"><span data-stu-id="a4c33-104">A [service control program](service-control-programs.md) can create or modify the DACL associated with a service to control access.</span></span> <span data-ttu-id="a4c33-105">Para recuperar a DACL associada a um objeto de serviço, use a função [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="a4c33-105">To retrieve the DACL associated with a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span> <span data-ttu-id="a4c33-106">Para definir a DACL, use a função [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="a4c33-106">To set the DACL, use the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="a4c33-107">As alterações feitas no [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associado ao objeto de serviço são persistentes até que o serviço seja removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4c33-107">Any changes made to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with the service object are persistent until the service is removed from the system.</span></span>

<span data-ttu-id="a4c33-108">O exemplo a seguir cria e define uma nova DACL para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a4c33-108">The following example creates and sets a new DACL for the service.</span></span> <span data-ttu-id="a4c33-109">O código mescla uma ACE (entrada de controle de acesso) à DACL existente para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a4c33-109">The code merges one access control entry (ACE) to the existing DACL for the service.</span></span> <span data-ttu-id="a4c33-110">A nova ACE concede ao serviço especificado o acesso de controle de início, parada, exclusão e leitura da conta de convidado \_ .</span><span class="sxs-lookup"><span data-stu-id="a4c33-110">The new ACE grants the Guest account start, stop, delete, and READ\_CONTROL access to the specified service.</span></span> <span data-ttu-id="a4c33-111">O acesso ao serviço pode ser modificado pelo parâmetro *AccessPermissions* passado para a função [**BuildExplicitAccessWithName**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea) .</span><span class="sxs-lookup"><span data-stu-id="a4c33-111">Access to the service can be modified by the *AccessPermissions* parameter passed to the [**BuildExplicitAccessWithName**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea) function.</span></span>

<span data-ttu-id="a4c33-112">A variável szSvcName é uma variável global que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="a4c33-112">The szSvcName variable is a global variable that contains the name of the service.</span></span> <span data-ttu-id="a4c33-113">Para obter o exemplo completo que define essa variável, consulte [SvcControl. cpp](svccontrol-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="a4c33-113">For the complete example that sets this variable, see [SvcControl.cpp](svccontrol-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Updates the service DACL to grant start, stop, delete, and read
//   control access to the Guest account.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoUpdateSvcDacl()
{
    EXPLICIT_ACCESS      ea;
    SECURITY_DESCRIPTOR  sd;
    PSECURITY_DESCRIPTOR psd            = NULL;
    PACL                 pacl           = NULL;
    PACL                 pNewAcl        = NULL;
    BOOL                 bDaclPresent   = FALSE;
    BOOL                 bDaclDefaulted = FALSE;
    DWORD                dwError        = 0;
    DWORD                dwSize         = 0;
    DWORD                dwBytesNeeded  = 0;

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service

    schService = OpenService( 
        schSCManager,              // SCManager database 
        szSvcName,                 // name of service 
        READ_CONTROL | WRITE_DAC); // access
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Get the current security descriptor.

    if (!QueryServiceObjectSecurity(schService,
        DACL_SECURITY_INFORMATION, 
        &psd,           // using NULL does not work on all versions
        0, 
        &dwBytesNeeded))
    {
        if (GetLastError() == ERROR_INSUFFICIENT_BUFFER)
        {
            dwSize = dwBytesNeeded;
            psd = (PSECURITY_DESCRIPTOR)HeapAlloc(GetProcessHeap(),
                    HEAP_ZERO_MEMORY, dwSize);
            if (psd == NULL)
            {
                // Note: HeapAlloc does not support GetLastError.
                printf("HeapAlloc failed\n");
                goto dacl_cleanup;
            }
  
            if (!QueryServiceObjectSecurity(schService,
                DACL_SECURITY_INFORMATION, psd, dwSize, &dwBytesNeeded))
            {
                printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
                goto dacl_cleanup;
            }
        }
        else 
        {
            printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
            goto dacl_cleanup;
        }
    }

    // Get the DACL.

    if (!GetSecurityDescriptorDacl(psd, &bDaclPresent, &pacl,
                                   &bDaclDefaulted))
    {
        printf("GetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Build the ACE.

    BuildExplicitAccessWithName(&ea, TEXT("GUEST"),
        SERVICE_START | SERVICE_STOP | READ_CONTROL | DELETE,
        SET_ACCESS, NO_INHERITANCE);

    dwError = SetEntriesInAcl(1, &ea, pacl, &pNewAcl);
    if (dwError != ERROR_SUCCESS)
    {
        printf("SetEntriesInAcl failed(%d)\n", dwError);
        goto dacl_cleanup;
    }

    // Initialize a new security descriptor.

    if (!InitializeSecurityDescriptor(&sd, 
        SECURITY_DESCRIPTOR_REVISION))
    {
        printf("InitializeSecurityDescriptor failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL in the security descriptor.

    if (!SetSecurityDescriptorDacl(&sd, TRUE, pNewAcl, FALSE))
    {
        printf("SetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL for the service object.

    if (!SetServiceObjectSecurity(schService, 
        DACL_SECURITY_INFORMATION, &sd))
    {
        printf("SetServiceObjectSecurity failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }
    else printf("Service DACL updated successfully\n");

dacl_cleanup:
    CloseServiceHandle(schSCManager);
    CloseServiceHandle(schService);

    if(NULL != pNewAcl)
        LocalFree((HLOCAL)pNewAcl);
    if(NULL != psd)
        HeapFree(GetProcessHeap(), 0, (LPVOID)psd);
}
```



## <a name="related-topics"></a><span data-ttu-id="a4c33-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4c33-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4c33-115">O exemplo de serviço completo</span><span class="sxs-lookup"><span data-stu-id="a4c33-115">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
