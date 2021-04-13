---
title: " no, size_is e out, size_is protótipo"
description: O protótipo de função a seguir usa duas cadeias de caracteres contadas. O desenvolvedor deve escrever código no cliente e no servidor para manter o controle dos comprimentos da matriz de caracteres e passar parâmetros que informam aos stubs quantos elementos de matriz devem ser transmitidos.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366593"
---
# <a name="in-size_is-and-out-size_is-prototype"></a><span data-ttu-id="51ef0-104">\[em, tamanho \_ é \] e \[ out, o tamanho \_ é \] protótipo</span><span class="sxs-lookup"><span data-stu-id="51ef0-104">\[in, size\_is\] and \[out, size\_is\] Prototype</span></span>

<span data-ttu-id="51ef0-105">O protótipo de função a seguir usa duas cadeias de caracteres contadas.</span><span class="sxs-lookup"><span data-stu-id="51ef0-105">The following function prototype uses two counted strings.</span></span> <span data-ttu-id="51ef0-106">O desenvolvedor deve escrever código no cliente e no servidor para manter o controle dos comprimentos da matriz de caracteres e passar parâmetros que informam aos stubs quantos elementos de matriz devem ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="51ef0-106">The developer must write code on both client and server to keep track of the character array lengths and pass parameters that tell the stubs how many array elements to transmit.</span></span>

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

<span data-ttu-id="51ef0-107">Observe que os parâmetros que descrevem o tamanho da matriz são transmitidos na mesma direção que as matrizes: *cbIn* e *achIn* estão \[ [**em**](/windows/desktop/Midl/in) \] parâmetros, enquanto *pcbOut* e *achOut* são parâmetros de \[ [**saída**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="51ef0-107">Note the parameters that describe the array length are transmitted in the same direction as the arrays: *cbIn* and *achIn* are \[[**in**](/windows/desktop/Midl/in)\] parameters while *pcbOut* and *achOut* are \[[**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="51ef0-108">Como um parâmetro **\[ \] out** , o parâmetro *PcbOut* deve seguir a Convenção C e ser declarado como um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="51ef0-108">As an **\[out\]** parameter, the parameter *pcbOut* must follow C convention and be declared as a pointer.</span></span>

<span data-ttu-id="51ef0-109">O código do cliente conta o número de caracteres na cadeia de caracteres, incluindo o zero à direita, antes de chamar o procedimento remoto, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="51ef0-109">The client code counts the number of characters in the string, including the trailing zero, before calling the remote procedure as shown:</span></span>

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

<span data-ttu-id="51ef0-110">O procedimento remoto no servidor fornece o comprimento do buffer de retorno em *cbOut* , conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="51ef0-110">The remote procedure on the server supplies the length of the return buffer in *cbOut* as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

<span data-ttu-id="51ef0-111">O \[ atributo de **cadeia de caracteres** \] pode ser utilizado quando um parâmetro é conhecido como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="51ef0-111">The \[**string**\] attribute can be utilized when a parameter is known to be a string.</span></span> <span data-ttu-id="51ef0-112">Esse atributo direciona o stub para calcular o tamanho da cadeia de caracteres, eliminando assim a sobrecarga associada ao \[ [**comprimento**](/windows/desktop/Midl/size-is) dos \] parâmetros.</span><span class="sxs-lookup"><span data-stu-id="51ef0-112">This attribute directs the stub to calculate the string size, thus eliminating the overhead associated with the \[[**length is**](/windows/desktop/Midl/size-is)\] parameters.</span></span> <span data-ttu-id="51ef0-113">Além disso, ele direcionará o stub para verificar se a cadeia de caracteres é terminada em **nulo** antes de passar o parâmetro para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51ef0-113">Additionally, it will direct the stub to verify the string is **NULL** terminated before passing the parameter to the application.</span></span>

 

 