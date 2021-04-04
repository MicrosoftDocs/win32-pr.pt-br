---
title: " dentro, fora do protótipo de cadeia de caracteres"
description: O protótipo de função a seguir usa um único parâmetro \ in, out, String \ para as cadeias de caracteres de entrada e saída.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917409"
---
# <a name="in-out-string-prototype"></a><span data-ttu-id="ab8ac-103">\[dentro, fora do protótipo de cadeia de caracteres \]</span><span class="sxs-lookup"><span data-stu-id="ab8ac-103">\[in, out, string\] Prototype</span></span>

<span data-ttu-id="ab8ac-104">O protótipo de função a seguir usa um único \[ parâmetro [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**String**](/windows/desktop/Midl/string) \] para as cadeias de caracteres de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="ab8ac-104">The following function prototype uses a single \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**string**](/windows/desktop/Midl/string)\] parameter for both the input and output strings.</span></span> <span data-ttu-id="ab8ac-105">A cadeia de caracteres contém primeiro a entrada de paciente e, em seguida, é substituída pela resposta médica, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="ab8ac-105">The string first contains patient input and is then overwritten with the doctor response as shown:</span></span>

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

<span data-ttu-id="ab8ac-106">Este exemplo é semelhante ao que empregava uma cadeia de caracteres de conta única para entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="ab8ac-106">This example is similar to the one that employed a single-counted string for both input and output.</span></span> <span data-ttu-id="ab8ac-107">Assim como no exemplo, o \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is) \] atributo determina o número de elementos alocados no servidor.</span><span class="sxs-lookup"><span data-stu-id="ab8ac-107">As with that example, the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute determines the number of elements allocated on the server.</span></span> <span data-ttu-id="ab8ac-108">O \[ [](/windows/desktop/Midl/string) \] atributo String direciona o stub para chamar **strlen** para determinar o número de elementos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="ab8ac-108">The \[[**string**](/windows/desktop/Midl/string)\] attribute directs the stub to call **strlen** to determine the number of transmitted elements.</span></span>

<span data-ttu-id="ab8ac-109">O cliente aloca toda a memória antes da chamada como:</span><span class="sxs-lookup"><span data-stu-id="ab8ac-109">The client allocates all memory before the call as:</span></span>

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

<span data-ttu-id="ab8ac-110">Observe que a função de análise não deve mais calcular o comprimento da cadeia de caracteres de retorno como fazia no exemplo de cadeia de caracteres contado, em que o atributo de **\[ cadeia de caracteres \]** não foi usado.</span><span class="sxs-lookup"><span data-stu-id="ab8ac-110">Note that the Analyze function no longer must calculate the length of the return string as it did in the counted-string example where the **\[string\]** attribute was not used.</span></span> <span data-ttu-id="ab8ac-111">Agora, os stubs calculam o comprimento conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="ab8ac-111">Now the stubs calculate the length as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 