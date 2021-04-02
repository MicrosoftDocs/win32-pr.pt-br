---
description: Enumera os certificados em um repositório de certificados, exibe o assunto e o usuário de cada certificado, e converte o nome da entidade de cada certificado em seu formato codificado de sua notação de sintaxe abstrata (ASN. 1) e, em seguida, de volta ao seu formulário decodificado.
ms.assetid: 8b4771da-0996-40fb-98ce-73efe8e3534f
title: 'Programa C de exemplo: convertendo nomes de certificados para ASN. 1 e voltar'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14114d4ba956acabf26ff28368403c699497b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829320"
---
# <a name="example-c-program-converting-names-from-certificates-to-asn1-and-back"></a>Programa C de exemplo: convertendo nomes de certificados para ASN. 1 e voltar

O exemplo a seguir enumera os certificados em um [*repositório de certificados*](../secgloss/c-gly.md), exibe o assunto e o usuário de cada certificado e converte o nome da entidade de cada certificado em seu formato codificado de sua [*notação de sintaxe abstrata*](../secgloss/a-gly.md) (ASN. 1) e, em seguida, de volta para seu formulário decodificado.

Este exemplo mostra as seguintes tarefas e funções de [*CryptoAPI*](../secgloss/c-gly.md) :

-   Abrir um armazenamento do sistema usando o [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).
-   Usando [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore) para obter o primeiro certificado do armazenamento aberto.
-   Usando [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para obter o nome da entidade e o nome de usuário do certificado.
-   Usando [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) para converter o nome da entidade do certificado em sua forma codificada de ASN. 1.
-   Usando [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea) para converter uma cadeia de caracteres codificada ASN. 1 em seu formulário decodificado.
-   Fechar um repositório de certificados usando [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) com o sinalizador sinalizador de **\_ \_ \_ verificação \_ do repositório próximo do certificado** .


```C++
#pragma comment(lib, "crypt32.lib")



//-------------------------------------------------------------------
// Example C Program: 
// Converting a name from a certificate to an ASN.1 encoded string
// and back.

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
#define MY_STRING_TYPE (CERT_OID_NAME_STR)

//-------------------------------------------------------------------
// Declare auxiliary functions

void MyHandleError(LPTSTR);
void Local_wait();

void main(void)
{
    HCERTSTORE hCertStore;
    PCCERT_CONTEXT pCertContext;

    //---------------------------------------------------------------
    // Begin Processing by opening a certificate store.

    if(!(hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        MY_ENCODING_TYPE,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"MY")))
    {
        MyHandleError(TEXT("The MY system store did not open."));
    }

    //---------------------------------------------------------------
    //       Loop through the certificates in the store. 
    //       For each certificate,
    //             get and print the name of the 
    //                  certificate subject and issuer.
    //             convert the subject name from the certificate
    //                  to an ASN.1 encoded string and print the
    //                  octets from that string.
    //             convert the encoded string back into its form 
    //                  in the certificate.

    pCertContext = NULL;
    while(pCertContext = CertEnumCertificatesInStore(
        hCertStore,
        pCertContext))
    {
        LPTSTR pszString;
        LPTSTR pszName;
        DWORD cbSize;
        CERT_BLOB blobEncodedName;

        //-----------------------------------------------------------
        //        Get and display 
        //        the name of subject of the certificate.

        if(!(cbSize = CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            0,
            NULL,   
            NULL,   
            0)))
        {
            MyHandleError(TEXT("CertGetName 1 failed."));
        }

        if(!(pszName = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        if(CertGetNameString(
            pCertContext,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszName,
            cbSize))

        {
            _tprintf(TEXT("\nSubject -> %s.\n"), pszName);

            //-------------------------------------------------------
            //       Free the memory allocated for the string.
            free(pszName);
        }
        else
        {
            MyHandleError(TEXT("CertGetName failed."));
        }

        //-----------------------------------------------------------
        //        Get and display 
        //        the name of Issuer of the certificate.

        if(!(cbSize = CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            CERT_NAME_ISSUER_FLAG,
            NULL,   
            NULL,   
            0)))
        {
            MyHandleError(TEXT("CertGetName 1 failed."));
        }

        if(!(pszName = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        if(CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            CERT_NAME_ISSUER_FLAG,
            NULL,   
            pszName,   
            cbSize))
        {
            _tprintf(TEXT("Issuer  -> %s.\n"), pszName);

            //-------------------------------------------------------
            //       Free the memory allocated for the string.
            free(pszName);
        }
        else
        {
            MyHandleError(TEXT("CertGetName failed."));
        }

        //-----------------------------------------------------------
        //       Convert the subject name to an ASN.1 encoded
        //       string and print the octets in that string.

        //       First : Get the number of bytes that must 
        //       be allocated for the string.

        cbSize = CertNameToStr(
            pCertContext->dwCertEncodingType,
            &(pCertContext->pCertInfo->Subject),
            MY_STRING_TYPE,
            NULL,
            0);

        //-----------------------------------------------------------
        //  The function CertNameToStr returns the number
        //  of bytes needed for a string to hold the
        //  converted name, including the null terminator. 
        //  If it returns one, the name is an empty string.

        if (1 == cbSize)
        {
            MyHandleError(TEXT("Subject name is an empty string."));
        }

        //-----------------------------------------------------------
        //        Allocated the needed buffer. Note that this
        //        memory must be freed inside the loop or the 
        //        application will leak memory.

        if(!(pszString = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        //-----------------------------------------------------------
        //       Call the function again to get the string. 

        cbSize = CertNameToStr(
            pCertContext->dwCertEncodingType,
            &(pCertContext->pCertInfo->Subject),
            MY_STRING_TYPE,
            pszString,
            cbSize);

        //-----------------------------------------------------------
        //  The function CertNameToStr returns the number
        //  of bytes in the string, including the null terminator.
        //  If it returns 1, the name is an empty string.

        if (1 == cbSize)
        {
            MyHandleError(TEXT("Subject name is an empty string."));
        }

        //-----------------------------------------------------------
        //    Get the length needed to convert the string back 
        //    back into the name as it was in the certificate.

        if(!(CertStrToName(
            MY_ENCODING_TYPE,
            pszString, 
            MY_STRING_TYPE,
            NULL,
            NULL,        // NULL to get the number of bytes 
                            // needed for the buffer.          
            &cbSize,     // Pointer to a DWORD to hold the 
                            // number of bytes needed for the 
                            // buffer
            NULL )))     // Optional address of a pointer to
                            // old the location for an error in the 
                            // input string.
        {
            MyHandleError(
                TEXT("Could not get the length of the BLOB."));
        }

        if (!(blobEncodedName.pbData = (LPBYTE)malloc(cbSize)))
        {
            MyHandleError(
                TEXT("Memory Allocation for the BLOB failed."));
        }
        blobEncodedName.cbData = cbSize;

        if(CertStrToName(
            MY_ENCODING_TYPE,
            pszString, 
            MY_STRING_TYPE,
            NULL,
            blobEncodedName.pbData,
            &blobEncodedName.cbData,
            NULL))
        {
            _tprintf(TEXT("CertStrToName created the BLOB.\n"));
        }
        else
        {
            MyHandleError(TEXT("Could not create the BLOB."));
        }

        //-----------------------------------------------------------
        //       Free the memory.

        free(blobEncodedName.pbData);
        free(pszString);

        //-----------------------------------------------------------
        //       Pause before information on the next certificate
        //       is displayed.

        Local_wait();

    } // End of while loop
     
    _tprintf(
        TEXT("\nThere are no more certificates in the store. \n"));

    //---------------------------------------------------------------
    //   Close the MY store.

    if(CertCloseStore(
        hCertStore,
        CERT_CLOSE_STORE_CHECK_FLAG))
    {
        _tprintf(TEXT("The store is closed. ")
            TEXT("All certificates are released.\n"));
    }
    else
    {
        _tprintf(TEXT("The store was closed, ")
            TEXT("but certificates still in use.\n"));
    }

    _tprintf(TEXT("This demonstration program ran to completion ")
        TEXT("without error.\n"));

    Local_wait();

} // End of main

//-------------------------------------------------------------------
//    This example uses the function MyHandleError, a simple error
//    handling function, to print an error message to the standard  
//    error (stderr) file and exit the program. 
//    For most applications, replace this function with one 
//    that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr,
        TEXT("An error occurred in running the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

void Local_wait()
{
//-------------------------------------------------------------------
//  This function prints a prompt string 
//  and wait for the user to hit enter.
//  It provides a pause with its length controlled by the user.

     _tprintf(TEXT("Hit Enter to continue : "));
     getchar();
}
```



 

 
