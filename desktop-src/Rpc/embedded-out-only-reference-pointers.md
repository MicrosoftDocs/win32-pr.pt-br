---
title: Ponteiros de referência de Out-Only inseridos
description: Ponteiros de referência de Out-Only inseridos
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36fc6229c0b155e3fa9a7f66e6cd1fbd742d7ec876264a8706ce81c4150d6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930501"
---
# <a name="embedded-out-only-reference-pointers"></a>Ponteiros de referência de Out-Only inseridos

Quando você usa \[ [](/windows/desktop/Midl/out-idl) \] ponteiros de referência somente out no Microsoft RPC, os stubs de servidor gerados alocam apenas o primeiro nível de ponteiros acessíveis a partir do ponteiro de referência. Os ponteiros em níveis mais detalhados não são alocados pelos stubs, mas devem ser alocados pela camada de aplicativo do servidor. Por exemplo, suponha que uma interface especifique uma \[  \] matriz somente out de ponteiros de referência:

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

Neste exemplo, o stub do servidor aloca memória para 10 ponteiros e define o valor de cada ponteiro como nulo. O aplicativo de servidor deve alocar a memória para os 10 inteiros [**curtos**](/windows/desktop/Midl/short) referenciados pelos ponteiros e, em seguida, definir os 10 ponteiros para apontarem para os inteiros.

Quando a \[ [](/windows/desktop/Midl/out-idl) \] estrutura de dados somente out inclui ponteiros de referência aninhados, os stubs de servidor alocam somente o primeiro ponteiro acessível do ponteiro de referência. Por exemplo:

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

No exemplo anterior, os stubs de servidor alocam o ponteiro *psTop* e **o \_ \_ tipo** de estrutura superior de struct. O ponteiro de referência *ps1* no **tipo de estrutura \_ superior \_** está definido como nulo. O stub do servidor não aloca todos os níveis da estrutura de dados, nem aloca o **\_ tipo STRUCT1** ou seu ponteiro incorporado, *psValue*.

 

 