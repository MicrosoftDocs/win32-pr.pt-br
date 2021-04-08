---
description: O exemplo a seguir demonstra como usar as funções CertOIDToAlgId e CertCompareIntegerBlob.
ms.assetid: 89186d98-80a9-460a-be2b-3e328675c485
title: 'Programa C de exemplo: usando CertOIDToAlgId e CertCompareIntegerBlob'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7239dc8872d1330cfd0dc96b00bcc201f94e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920985"
---
# <a name="example-c-program-using-certoidtoalgid-and-certcompareintegerblob"></a><span data-ttu-id="d668f-103">Programa C de exemplo: usando CertOIDToAlgId e CertCompareIntegerBlob</span><span class="sxs-lookup"><span data-stu-id="d668f-103">Example C Program: Using CertOIDToAlgId and CertCompareIntegerBlob</span></span>

<span data-ttu-id="d668f-104">O exemplo a seguir demonstra como usar as funções [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid) e [**CertCompareIntegerBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob) .</span><span class="sxs-lookup"><span data-stu-id="d668f-104">The following example demonstrates using the [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid) and [**CertCompareIntegerBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob) functions.</span></span>

<span data-ttu-id="d668f-105">Primeiro, todos os OIDs disponíveis são enumerados usando [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo).</span><span class="sxs-lookup"><span data-stu-id="d668f-105">First, all available OIDs are enumerated using [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo).</span></span> <span data-ttu-id="d668f-106">O código usado com essa função também demonstra o uso de uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d668f-106">Code used with this function also demonstrates the use of a callback function.</span></span> <span data-ttu-id="d668f-107">A função de retorno de chamada demonstra a lógica de interrupção para pausar entre cada grupo de OID e depois de apresentar informações sobre um número definido de OIDs.</span><span class="sxs-lookup"><span data-stu-id="d668f-107">The callback function demonstrates break logic to pause between each OID group and after presenting information on a set number of OIDs.</span></span>

<span data-ttu-id="d668f-108">Segundo, as três cadeias de caracteres de OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) são convertidas em números inteiros de identificador de algoritmo **DWORD** usando [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid).</span><span class="sxs-lookup"><span data-stu-id="d668f-108">Second, three [*object identifier*](../secgloss/o-gly.md) (OID) strings are converted into **DWORD** algorithm identifier integers using [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid).</span></span> <span data-ttu-id="d668f-109">O código também demonstra que todas as cadeias de caracteres de OID não têm identificadores de algoritmo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d668f-109">The code also demonstrates that all OID strings do not have related algorithm identifiers.</span></span>

<span data-ttu-id="d668f-110">Por fim, o exemplo demonstra a comparação de BLOBs inteiros.</span><span class="sxs-lookup"><span data-stu-id="d668f-110">Finally, the example demonstrates comparing integer BLOBs.</span></span> <span data-ttu-id="d668f-111">Este exemplo demonstra o truncamento de 0x00's à esquerda de números positivos e 0xFF's à esquerda de números negativos.</span><span class="sxs-lookup"><span data-stu-id="d668f-111">This example demonstrates the truncation of leading 0x00's from positive numbers and leading 0xFF's from negative numbers.</span></span>

<span data-ttu-id="d668f-112">Ele também mostra que os inteiros são comparados como se estivessem armazenados no formato [*little-endian*](../secgloss/l-gly.md) com os dígitos mais significativos à direita.</span><span class="sxs-lookup"><span data-stu-id="d668f-112">It also shows that integers are compared as though they are stored in [*little-endian*](../secgloss/l-gly.md) form with the most significant digits on the right.</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare a wait function to be defined following main.

void my_wait(char *s);

//-------------------------------------------------------------------
// Callback function to print information
// saved in each CRYPT_OID_INFO structure.
// This function counts the number of lines printed
// and does a wait for each new ground and after any four
// report groups are printed.

static BOOL WINAPI EnumInfoCallback(
     PCCRYPT_OID_INFO pInfo,
     void *pvArg
    )
{
static int old_oid = 0;
static int break_counter = 0;

if( old_oid < pInfo->dwGroupId)
{
     if(old_oid > 0)
     {
          my_wait("\n Begin new group. \n Hit enter to continue.");
          break_counter=0;
     }
     old_oid = pInfo->dwGroupId;
     printf("\nNew Group ID %d \n",old_oid);
}
printf("  OID: %s\n  Name: %S\n",
       pInfo->pszOID, pInfo->pwszName);

//-------------------------------------------------------------------
// If there is an AlgId, print it.

if( pInfo->Algid > 0)
{
     printf("  Algorithm ID hexadecimal %x \n\n",pInfo->Algid);
}
else
{
     printf("\n");
}

if(++break_counter > 4)
{ 
     break_counter = 0;
     my_wait("\n   Hit enter to continue.");
}
return TRUE;
}

void main()
{
//-------------------------------------------------------------------
// Note: Integer BLOBs are treated as if they
// are stored in little-endian form with the 
// most significant digits on the right. Truncation is 
// therefore from the right.
// Integer BLOBs are also assumed to be signed numbers
// in two's compliment form.
// For negative numbers, 0xFFs on the right are 
// truncated.
// For positive numbers, 0x00s on the right are 
// truncated.

//-------------------------------------------------------------------
// Declare and initialize local variables.

DWORD Alg_Id;
CRYPT_INTEGER_BLOB  Int1, Int2;
BYTE BLOB1data[4] = {0x88, 0xFF, 0xFF, 0xFF};
BYTE BLOB2data[2] = {0x88, 0xFF};
BYTE BLOB3data[4] = {0x01, 0x00, 0x00, 0x00};
BYTE BLOB4data[2] = {0x01, 0x00};
BYTE BLOB5data[4] = {0x01, 0x00, 0x01, 0x00};

//-------------------------------------------------------------------
// Enumerate the algorithm OIDs available.
// Note that this one call to the function with
// dwGroupId set to 0 lists all OIDs in all groups. 

if(!(CryptEnumOIDInfo(
    0,                  // use 0 to enumerate the OIDs in all groups
    0,                  // dwFlags
    NULL,               // no additional parameters are to be 
                        // passed to the callback function.
    EnumInfoCallback    // name of the callback function to be 
                        // called for each OID enumerated.
    )))
{
    printf("Enumeration of algorithm OIDs did not complete.\n");
}

//-------------------------------------------------------------------
// Use CertOIDToAlgId() to 
// convert the szOID_RSA_RC4 Object Identifier string to an 
// algorithm identifier.

if( Alg_Id = CertOIDToAlgId(szOID_RSA_RC4))
{
   // Print the Alg_Id returned in hex.
   printf("szOID_RSA_RC4 / %s is %x\n\n",szOID_RSA_RC4, Alg_Id);
}
else
{
   printf("No ALG_ID for OID szOID_RSA_RC4 / %s.\n", szOID_RSA_RC4);
}

//-------------------------------------------------------------------
// Convert the szOID_RSA_RC2CBC Object Identifier string to an 
// algorithm identifier.

if( Alg_Id = CertOIDToAlgId(szOID_RSA_RC2CBC))
{
   // Print the Alg_Id returned in hex.
   printf("szOID_RSA_RC2CBC / %s is %x\n\n",szOID_RSA_RC2CBC, 
      Alg_Id);
}
else
{
   printf("No ALG_ID for szOID_RSA_RC2CBC / %s.\n",szOID_RSA_RC2CBC);
}

//-------------------------------------------------------------------
// Convert the szOID_RSA_RC5_CBCPad Object Identifier string to an 
// algorithm identifier.

if( Alg_Id = CertOIDToAlgId(szOID_RSA_RC5_CBCPad))
{
   // Print the Alg_Id returned in hex.
   printf("szOID_RSA_RC5_CBCPad / %s is %x\n",szOID_RSA_RC5_CBCPad, 
      Alg_Id);
}
else
{
    printf("No ALG_ID for szOID_RSA_RC5_CBCPad: %s.\n",
      szOID_RSA_RC5_CBCPad);
}

//-------------------------------------------------------------------
// Initialize Int1 and Int2. 

Int1.pbData = (BYTE*)&BLOB1data;
Int2.pbData = (BYTE*)&BLOB2data;

//-------------------------------------------------------------------
// Set the cbData members so that only 
// the leftmost two bytes of the 
// first are compared to the leftmost bytes 
// of the second.

Int1.cbData = 4;  // sizeof(BLOB1data);
Int2.cbData = 2;  // sizeof(BLOB2data);

if( CertCompareIntegerBlob(
     &Int1, 
     &Int2))
{
   printf("The first two bytes of the BLOBs are identical.\n");
}
else
{
   printf("The first two bytes BLOBs are not identical.\n");
}

//-------------------------------------------------------------------
// Reset the cbData members to compare only 
// 1 byte from each.

Int1.cbData=1;
Int2.cbData=1;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
    printf("The BLOBs of different length are identical.\n");
}
else
{
    printf("The BLOBs of different length are not identical.\n");
}

//-------------------------------------------------------------------
// Reset to check the positive numbers.

Int1.cbData = 4;
Int2.cbData = 2;
Int1.pbData = BLOB3data;
Int2.pbData = BLOB4data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("The BLOBs 3 and 4 are identical.\n");
}
else
{
   printf("The BLOBs 3 and 4 are not identical.\n");
}

//-------------------------------------------------------------------
// Compare BLOB 1 and BLOB 3.

Int1.cbData = 4;
Int2.cbData = 4;
Int1.pbData = BLOB1data;
Int2.pbData = BLOB3data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("BLOBs 1 and 3 are identical.\n");
}
else
{
   printf("BLOBs 1 and 3 are not identical.\n");
}

//-------------------------------------------------------------------
// Compare BLOB 3 and BLOB 5.

Int1.cbData = 4;
Int2.cbData = 4;
Int1.pbData = BLOB5data;
Int2.pbData = BLOB3data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("BLOBs 5 and 3 are identical.\n");
}
else
{
   printf("BLOBs 5 and 3 are not identical.\n");
}

//-------------------------------------------------------------------
// Compare the first two bytes of BLOB 3 and BLOB 5.

Int1.cbData = 2;
Int2.cbData = 2;
Int1.pbData = BLOB5data;
Int2.pbData = BLOB3data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("The first two bytes of BLOBs 5 and 3 are identical.\n");
}
else
{
   printf("The first two bytes of BLOBs 5 and 3 not identical.\n");
}
} // end main

//-------------------------------------------------------------------
// Define the my_wait function.
void my_wait(char* s)
{
     printf(s);
     getchar();
}
```



 

 
