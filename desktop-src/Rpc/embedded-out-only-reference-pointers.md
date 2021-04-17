---
title: Ponteiros de referência de Out-Only inseridos
description: Ponteiros de referência de Out-Only inseridos
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759599"
---
# <a name="embedded-out-only-reference-pointers"></a><span data-ttu-id="77b9e-103">Ponteiros de referência de Out-Only inseridos</span><span class="sxs-lookup"><span data-stu-id="77b9e-103">Embedded Out-Only Reference Pointers</span></span>

<span data-ttu-id="77b9e-104">Quando você usa \[ [](/windows/desktop/Midl/out-idl) \] ponteiros de referência somente out no Microsoft RPC, os stubs de servidor gerados alocam apenas o primeiro nível de ponteiros acessíveis a partir do ponteiro de referência.</span><span class="sxs-lookup"><span data-stu-id="77b9e-104">When you use \[[**out**](/windows/desktop/Midl/out-idl)\]-only reference pointers in Microsoft RPC, the generated server stubs allocate only the first level of pointers accessible from the reference pointer.</span></span> <span data-ttu-id="77b9e-105">Os ponteiros em níveis mais detalhados não são alocados pelos stubs, mas devem ser alocados pela camada de aplicativo do servidor.</span><span class="sxs-lookup"><span data-stu-id="77b9e-105">Pointers at deeper levels are not allocated by the stubs, but must be allocated by the server application layer.</span></span> <span data-ttu-id="77b9e-106">Por exemplo, suponha que uma interface especifique uma \[  \] matriz somente out de ponteiros de referência:</span><span class="sxs-lookup"><span data-stu-id="77b9e-106">For example, suppose an interface specifies an \[**out**\]-only array of reference pointers:</span></span>

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

<span data-ttu-id="77b9e-107">Neste exemplo, o stub do servidor aloca memória para 10 ponteiros e define o valor de cada ponteiro como nulo.</span><span class="sxs-lookup"><span data-stu-id="77b9e-107">In this example, the server stub allocates memory for 10 pointers and sets the value of each pointer to null.</span></span> <span data-ttu-id="77b9e-108">O aplicativo de servidor deve alocar a memória para os 10 inteiros [**curtos**](/windows/desktop/Midl/short) referenciados pelos ponteiros e, em seguida, definir os 10 ponteiros para apontarem para os inteiros.</span><span class="sxs-lookup"><span data-stu-id="77b9e-108">The server application must allocate the memory for the 10 [**short**](/windows/desktop/Midl/short) integers referenced by the pointers and then set the 10 pointers to point to the integers.</span></span>

<span data-ttu-id="77b9e-109">Quando a \[ [](/windows/desktop/Midl/out-idl) \] estrutura de dados somente out inclui ponteiros de referência aninhados, os stubs de servidor alocam somente o primeiro ponteiro acessível do ponteiro de referência.</span><span class="sxs-lookup"><span data-stu-id="77b9e-109">When the \[[**out**](/windows/desktop/Midl/out-idl)\]-only data structure includes nested reference pointers, the server stubs allocate only the first pointer accessible from the reference pointer.</span></span> <span data-ttu-id="77b9e-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="77b9e-110">For example:</span></span>

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

<span data-ttu-id="77b9e-111">No exemplo anterior, os stubs de servidor alocam o ponteiro *psTop* e **o \_ \_ tipo** de estrutura superior de struct.</span><span class="sxs-lookup"><span data-stu-id="77b9e-111">In the preceding example, the server stubs allocate the pointer *psTop* and the structure **STRUCT\_TOP\_TYPE**.</span></span> <span data-ttu-id="77b9e-112">O ponteiro de referência *ps1* no **tipo de estrutura \_ superior \_** está definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="77b9e-112">The reference pointer *ps1* in **STRUCT\_TOP\_TYPE** is set to null.</span></span> <span data-ttu-id="77b9e-113">O stub do servidor não aloca todos os níveis da estrutura de dados, nem aloca o **\_ tipo STRUCT1** ou seu ponteiro incorporado, *psValue*.</span><span class="sxs-lookup"><span data-stu-id="77b9e-113">The server stub does not allocate every level of the data structure, nor does it allocate the **STRUCT1\_TYPE** or its embedded pointer, *psValue*.</span></span>

 

 