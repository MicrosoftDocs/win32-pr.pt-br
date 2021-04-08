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
# <a name="retrieving-data-of-unknown-length"></a>Recuperando dados de comprimento desconhecido

Muitas funções retornam uma quantidade potencialmente grande de dados para um endereço fornecido como um dos parâmetros pelo aplicativo. Em todos esses casos, a operação é executada de maneira semelhante, se não idêntica. O parâmetro que aponta para o local dos dados retornados usará a Convenção de notação, em que PB ou VP são os dois primeiros caracteres do nome do parâmetro. Outro parâmetro terá PCB como os três primeiros caracteres do nome do parâmetro. Esse parâmetro representa o tamanho, em bytes, dos dados que serão retornados para o local PB ou VP. Por exemplo, considere a seguinte especificação de função:

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

Neste exemplo, *pbData* é um ponteiro para o local onde os dados serão retornados e *pcbData* é o tamanho, em bytes, dos dados retornados.

> [!Note]  
> Às vezes, o parâmetro Companion para o parâmetro PCB pode transportar um prefixo ligeiramente diferente, como p ou PV. Além disso, para os parâmetros complementares usando a combinação de prefixos PWSZ e PCCh, o parâmetro PCCh é a contagem, em caracteres ([*Unicode*](../secgloss/u-gly.md) ou [*ASCII*](../secgloss/a-gly.md), conforme aplicável), dos dados retornados.

 

Se o buffer especificado pelo parâmetro *pbData* não for grande o suficiente para manter os dados retornados, a função definirá o erro de \_ mais \_ código de dados (que pode ser visto chamando a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) e armazenará o tamanho de buffer necessário, em bytes, na variável apontada por *pcbData*.

Se **NULL** for entrada para *pbData* e *pcbData* não for **NULL**, nenhum erro será retornado e a função retornará o tamanho, em bytes, do buffer de memória necessário na variável apontada por *pcbData*. Isso permite que um aplicativo determine o tamanho de e a melhor maneira de alocar um buffer para os dados retornados.

> [!Note]  
> Quando **NULL** é entrada para *pbData* para determinar o tamanho necessário para garantir que os dados retornados caibam no buffer especificado, a segunda chamada para a função que popula o buffer com os dados desejados pode não usar o buffer inteiro. Após a segunda chamada, o tamanho real dos dados retornados está contido em *pcbData*. Use esse tamanho ao processar os dados.

 

O exemplo a seguir mostra como os parâmetros de entrada e saída podem ser implementados para essa finalidade.


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



 

 
