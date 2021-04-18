---
description: Explica como usar o CryptoAPI para gerenciar e verificar certificados.
ms.assetid: 1c26509d-5bb6-42dc-aeb0-525d7eaecf7d
title: 'Programa C de exemplo: operações de verificação de certificado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efdbaaea172b24448ad2b15b03ee19c6dc7a445
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751316"
---
# <a name="example-c-program-certificate-verification-operations"></a><span data-ttu-id="cf5aa-103">Programa C de exemplo: operações de verificação de certificado</span><span class="sxs-lookup"><span data-stu-id="cf5aa-103">Example C Program: Certificate Verification Operations</span></span>

<span data-ttu-id="cf5aa-104">O exemplo a seguir ilustra essas tarefas e funções de CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="cf5aa-104">The following example illustrates these tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="cf5aa-105">Abrir e fechar o repositório do sistema.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-105">Opening and closing the system store.</span></span>
-   <span data-ttu-id="cf5aa-106">Localizando um certificado pelo nome da entidade.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-106">Finding a certificate by subject name.</span></span>
-   <span data-ttu-id="cf5aa-107">Usando a função [**CertVerifyTimeValidity**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity) para verificar a validade da hora do certificado.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-107">Using the [**CertVerifyTimeValidity**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity) function to check the certificate's time validity.</span></span>
-   [<span data-ttu-id="cf5aa-108">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-108">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
-   [<span data-ttu-id="cf5aa-109">**CertFindCertificateInStore**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-109">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
-   [<span data-ttu-id="cf5aa-110">**CertVerifyTimeValidity**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-110">**CertVerifyTimeValidity**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity)
-   [<span data-ttu-id="cf5aa-111">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-111">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)
-   [<span data-ttu-id="cf5aa-112">**CertCloseStore**</span><span class="sxs-lookup"><span data-stu-id="cf5aa-112">**CertCloseStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

<span data-ttu-id="cf5aa-113">Este exemplo usa a função [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="cf5aa-113">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="cf5aa-114">O código para essa função está incluído no exemplo.</span><span class="sxs-lookup"><span data-stu-id="cf5aa-114">The code for this function is included with the sample.</span></span> <span data-ttu-id="cf5aa-115">O código para essa e outras funções auxiliares também está listado em [funções uso geral](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cf5aa-115">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
//  Copyright (C) Microsoft.  All rights reserved.
//  This example demonstrates: 
//      1. Opening and closing a system store.
//      2. Finding a certificate by subject name.
//      3. Using the CertVerifyTimeValidity function to check the 
//                certificate's time validity.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE      hSystemStore;
PCCERT_CONTEXT  pTargetCert=NULL;
PCERT_INFO      pTargetCertInfo; 
char            szSubjectName[] = "Insert_cert_subject_name1"; 
                      // String to be found in a certificate subject

//-------------------------------------------------------------------
// Call CertOpenStore to open the CA store.

if(hSystemStore = CertOpenStore(
      CERT_STORE_PROV_SYSTEM,
      0,
      NULL, 
      CERT_SYSTEM_STORE_CURRENT_USER,
      L"CA"))
{
   printf("CertOpenStore succeeded. The CA store is open. \n");
}
else
{
   MyHandleError( "Error opening the Root store.");
}
//-------------------------------------------------------------------
// Get a particular certificate using CertFindCertificateInStore.

if(pTargetCert = CertFindCertificateInStore(
      hSystemStore,           // Store handle.
      MY_ENCODING_TYPE,       // Encoding type.
      0,                      // Not used.
      CERT_FIND_SUBJECT_STR_A,// Find type. Find a string in the 
                              // certificate's subject.
      szSubjectName,          // The string to be searched for.
      pTargetCert))           // Previous context.
{
   printf("Found the certificate. \n");
}
else
{
   MyHandleError("Could not find the required certificate");
}
//-------------------------------------------------------------------
// pTargetCert is a pointer to the desired certificate.
// Check the certificate's time validity.

pTargetCertInfo = pTargetCert->pCertInfo;    
switch(CertVerifyTimeValidity(
      NULL,               // Use current time.
      pTargetCertInfo))   // Pointer to CERT_INFO.
{
   case -1 :
   {
        printf("Certificate is not valid yet. \n");
        break;
   }
   case 1:
   {
       printf("Certificate is expired. \n");
       break;
   }
   case 0:
   {
      printf("Certificate's time is valid. \n");
      break;
    }
};
//-------------------------------------------------------------------
// Clean up memory and quit.

if (pTargetCert)
   CertFreeCertificateContext(pTargetCert);
if(hSystemStore)
{
   if (!CertCloseStore(
       hSystemStore, 
       CERT_CLOSE_STORE_CHECK_FLAG))
       MyHandleError("Could not close the certificate store");
}
printf("The certificate has been freed and the store closed. \n");
printf("The certificate verification program ran to completion "
       "without error. \n");
} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 



