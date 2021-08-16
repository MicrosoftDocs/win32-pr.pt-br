---
description: Mostra o registro (criação) e a abertura de um armazenamento do sistema, o registro de um armazenamento físico como membro de um armazenamento do sistema e o registro (exclusão) de um armazenamento do sistema.
ms.assetid: 857ab592-68c7-4660-b37d-b165aeee14f4
title: 'Exemplo de programa C: registrando armazenamentos de certificados físicos e do sistema'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3e1302f0590244ae4e1cd84e477c5deac8266b69d15f9ee83f60b71df3d1a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140869"
---
# <a name="example-c-program-registering-physical-and-system-certificate-stores"></a>Exemplo de programa C: registrando armazenamentos de certificados físicos e do sistema

Os armazenamentos físicos podem se tornar membros mais ou menos permanentes de um armazenamento do sistema. Quando um armazenamento físico for membro de um armazenamento do sistema, as operações no armazenamento do sistema, como localizar um certificado, procurarão em todos os armazenamentos físicos registrados como membros do armazenamento do sistema. Um armazenamento físico pode ser removido da associação em um armazenamento do sistema usando uma função de registro.

Este exemplo mostra as seguintes tarefas e funções CryptoAPI:

-   Registrando (criando) um novo repositório de sistema usando [**CertRegisterSystemStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)
-   Abrir um repositório de sistema recém-criado [**usando CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
-   Registrar um repositório físico como membro de um repositório do sistema usando [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).
-   Não registro (exclusão) de um repositório do sistema usando [**CertUnregisterSystemStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)

Este exemplo também demonstra a criação e a exclusão de armazenamentos do sistema.


```C++
// This example uses CertRegisterSystemStore.
#pragma comment(lib, "crypt32.lib")

// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main()
{


// Declare and initialize variables.

HCERTSTORE hSystemStore;
DWORD dwFlags= CERT_SYSTEM_STORE_CURRENT_USER;
LPCWSTR pvSystemName= L"NEWSTORE";  // For this setting of 
                                    // dwFlags, the store name may 
                                    // be prefixed with a user name.
CERT_PHYSICAL_STORE_INFO PhysicalStoreInfo;
BYTE fResponse  = 'n';

if(CertRegisterSystemStore(
    pvSystemName,
    dwFlags,
    NULL,
    NULL))
  printf("System store %S is registered. \n",pvSystemName);
else
  printf("The system store did not register. \n");


// Open the NEWSTORE as a system store.

if(hSystemStore = CertOpenStore(
   CERT_STORE_PROV_SYSTEM,   // the store provider type
   0,                        // the encoding type is not needed
   NULL,                     // use the default HCRYPTPROV
   CERT_SYSTEM_STORE_CURRENT_USER,
                             // set the store location in a registry
                             // location
   pvSystemName ))           // the store name as a Unicode string
{
     printf("The new store has been opened as a system store.\n");
}
else
{
     printf("The new store was not opened as a system store.\n");
}
if(hSystemStore)
{
    if(CertCloseStore(hSystemStore,0))
    {
        printf("The system store has been closed.\n");
    }
    else
    {
        printf("The system store could not be closed.\n");
    }
}
else
{
   printf("The system store did not need to be closed.\n");
}


// Initialize PhysicalStoreInfo.

PhysicalStoreInfo.cbSize=sizeof(CERT_PHYSICAL_STORE_INFO);
PhysicalStoreInfo.pszOpenStoreProvider=(LPSTR)
    CERT_STORE_PROV_FILENAME;
PhysicalStoreInfo.dwFlags=CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG;


// Replace the path below with one that is appropriate for you.

PhysicalStoreInfo.OpenParameters.pbData = 
    (BYTE *) L"C:\\temp\\mystore";
PhysicalStoreInfo.OpenParameters.cbData = 
    (wcslen((LPWSTR) PhysicalStoreInfo.OpenParameters.pbData) + 1) * 
    sizeof(WCHAR);

PhysicalStoreInfo.dwPriority=1;
PhysicalStoreInfo.dwOpenEncodingType=MY_ENCODING_TYPE;


// Register the physical store.

if(CertRegisterPhysicalStore(
      L"NEWSTORE",
      dwFlags,
      L"TESTOR.STO",
      &PhysicalStoreInfo,
      NULL
      ))
{
       printf("Physical store is registered. \n");
}
else
{
       printf("The physical store was not registered.\n");
}  


//  Next, unregister the store.

printf("Would you like to unregister the %S store? (y/n) "
       ,pvSystemName);
scanf_s("%c",&fResponse);

if(fResponse=='y')
{
   if(CertUnregisterSystemStore(
     pvSystemName,
     dwFlags))
   {
      printf("System store %S has been unregistered.\n"
          ,pvSystemName);
   }
   else
   {
      printf("The system store was not unregistered.\n");
   }
}
}  // end main


//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to  
//  the standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end of MyHandleError
```



 

 



