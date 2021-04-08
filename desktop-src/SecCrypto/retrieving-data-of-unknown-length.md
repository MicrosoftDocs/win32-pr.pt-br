---
description: Muitas funções retornam uma quantidade potencialmente grande de dados para um endereço fornecido como um dos parâmetros pelo aplicativo.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Recuperando dados de comprimento desconhecido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30620018f3c4871bd27299c3dd21ae42936c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827761"
---
# <a name="retrieving-data-of-unknown-length"></a><span data-ttu-id="a261c-103">Recuperando dados de comprimento desconhecido</span><span class="sxs-lookup"><span data-stu-id="a261c-103">Retrieving Data of Unknown Length</span></span>

<span data-ttu-id="a261c-104">Muitas funções retornam uma quantidade potencialmente grande de dados para um endereço fornecido como um dos parâmetros pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a261c-104">Many functions return a potentially large amount of data to an address provided as one of the parameters by the application.</span></span> <span data-ttu-id="a261c-105">Em todos esses casos, a operação é executada de maneira semelhante, se não idêntica.</span><span class="sxs-lookup"><span data-stu-id="a261c-105">In all these cases, the operation is performed in a similar, if not identical, fashion.</span></span> <span data-ttu-id="a261c-106">O parâmetro que aponta para o local dos dados retornados usará a Convenção de notação, em que PB ou VP são os dois primeiros caracteres do nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a261c-106">The parameter that points to the location of the returned data will use the notation convention where pb or pv are the first two characters of the parameter name.</span></span> <span data-ttu-id="a261c-107">Outro parâmetro terá PCB como os três primeiros caracteres do nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a261c-107">Another parameter will have pcb as the first three characters of the parameter name.</span></span> <span data-ttu-id="a261c-108">Esse parâmetro representa o tamanho, em bytes, dos dados que serão retornados para o local PB ou VP.</span><span class="sxs-lookup"><span data-stu-id="a261c-108">This parameter represents the size, in bytes, of the data that will be returned to the pb or pv location.</span></span> <span data-ttu-id="a261c-109">Por exemplo, considere a seguinte especificação de função:</span><span class="sxs-lookup"><span data-stu-id="a261c-109">For example, consider the following function specification:</span></span>

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

<span data-ttu-id="a261c-110">Neste exemplo, *pbData* é um ponteiro para o local onde os dados serão retornados e *pcbData* é o tamanho, em bytes, dos dados retornados.</span><span class="sxs-lookup"><span data-stu-id="a261c-110">In this example, *pbData* is a pointer to the location where the data will be returned, and *pcbData* is the size, in bytes, of the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="a261c-111">Às vezes, o parâmetro Companion para o parâmetro PCB pode transportar um prefixo ligeiramente diferente, como p ou PV.</span><span class="sxs-lookup"><span data-stu-id="a261c-111">The companion parameter to the pcb parameter may sometimes carry a slightly different prefix, such as p or pv.</span></span> <span data-ttu-id="a261c-112">Além disso, para os parâmetros complementares usando a combinação de prefixos PWSZ e PCCh, o parâmetro PCCh é a contagem, em caracteres ([*Unicode*](../secgloss/u-gly.md) ou [*ASCII*](../secgloss/a-gly.md), conforme aplicável), dos dados retornados.</span><span class="sxs-lookup"><span data-stu-id="a261c-112">Also, for companion parameters using the combination of prefixes pwsz and pcch, the pcch parameter is the count, in characters ([*Unicode*](../secgloss/u-gly.md) or [*ASCII*](../secgloss/a-gly.md), as applicable), of the returned data.</span></span>

 

<span data-ttu-id="a261c-113">Se o buffer especificado pelo parâmetro *pbData* não for grande o suficiente para manter os dados retornados, a função definirá o erro de \_ mais \_ código de dados (que pode ser visto chamando a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) e armazenará o tamanho de buffer necessário, em bytes, na variável apontada por *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="a261c-113">If the buffer specified by the *pbData* parameter is not large enough to hold the returned data, the function sets the ERROR\_MORE\_DATA code (which can be seen by calling the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function) and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*.</span></span>

<span data-ttu-id="a261c-114">Se **NULL** for entrada para *pbData* e *pcbData* não for **NULL**, nenhum erro será retornado e a função retornará o tamanho, em bytes, do buffer de memória necessário na variável apontada por *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="a261c-114">If **NULL** is input for *pbData* and *pcbData* is not **NULL**, no error is returned, and the function returns the size, in bytes, of the needed memory buffer in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="a261c-115">Isso permite que um aplicativo determine o tamanho de e a melhor maneira de alocar um buffer para os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="a261c-115">This lets an application determine the size of, and the best way to allocate, a buffer for the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="a261c-116">Quando **NULL** é entrada para *pbData* para determinar o tamanho necessário para garantir que os dados retornados caibam no buffer especificado, a segunda chamada para a função que popula o buffer com os dados desejados pode não usar o buffer inteiro.</span><span class="sxs-lookup"><span data-stu-id="a261c-116">When **NULL** is input for *pbData* to determine the size needed to ensure that the returned data fits in the specified buffer, the second call to the function which populates the buffer with the desired data may not use the whole buffer.</span></span> <span data-ttu-id="a261c-117">Após a segunda chamada, o tamanho real dos dados retornados está contido em *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="a261c-117">After the second call, the actual size of the data returned is contained in *pcbData*.</span></span> <span data-ttu-id="a261c-118">Use esse tamanho ao processar os dados.</span><span class="sxs-lookup"><span data-stu-id="a261c-118">Use this size when processing the data.</span></span>

 

<span data-ttu-id="a261c-119">O exemplo a seguir mostra como os parâmetros de entrada e saída podem ser implementados para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="a261c-119">The following example shows how input and output parameters might be implemented for this purpose.</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(char *s);

void main()
{

// Set up SomeFunction variables.
PCCRL_CONTEXT pCrlContext; // Initialized elsewhere.
DWORD dwPropId;            // Initialized elsewhere.
DWORD cbData;
BYTE  *pbData;

// Call SomeFunction to set cbData, the size of 
// the buffer needed for pbData.
if(SomeFunction(
     pCrlContext, 
     dwPropId, 
     NULL, 
     &cbData))
{
       printf("The function succeeded.\n");
}
else
{

// The function call failed. Handle the error.
       MyHandleError("Function call failed.");
}

// The call succeeded; the size for the needed buffer, in bytes, 
// now resides in cbData.

// Malloc memory for the size of the message.
if(pbData = (BYTE*)malloc(cbData))
{
   printf("Memory has been allocated.\n");
}
else
{

   // The allocation failed. Write an error message and exit.
   MyHandleError("Malloc operation failed. ");
}

// The space for the buffer has been allocated.
// Call SomeFunction to fill the buffer with the data.
if(SomeFunction(
      pCrlContext, 
      dwPropId, 
      pbData, 
      &cbData))
{
       printf("The function succeeded.\n");
}
else
{

   // The second function call failed. Handle the error.
   MyHandleError("The second call to the function failed.");
}

// The function succeeded; the data is now in the buffer
// pointed to by pbData. Note that cbData is
// updated with the actual size of the data returned. Use this size 
// to process bytes of pbData.

// When you have finished using the allocated memory, free it.
free(pbData);

} // End of main

//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.
void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
}
```



 

 
