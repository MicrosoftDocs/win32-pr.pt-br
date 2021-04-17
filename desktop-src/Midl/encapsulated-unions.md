---
title: Uniões encapsuladas
description: Uma União que está contida com seu discriminante em uma estrutura dentro do é uma União encapsulada.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- tipos de dados MIDL, uniões encapsuladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789783"
---
# <a name="encapsulated-unions"></a>Uniões encapsuladas

Uma União que está contida com seu discriminante em uma estrutura dentro do é uma União encapsulada. A União encapsulada é indicada pela presença da palavra-chave [**switch**](switch.md) . Esse tipo de União é tão nomeado porque o compilador MIDL encapsula automaticamente a União e seu discriminante em uma estrutura para transmissão durante uma chamada de procedimento remoto.

Se a marca Union estiver ausente (U1 \_ Type no exemplo acima), o compilador irá gerar a estrutura com o campo Union chamado *\_ Union marcada*.

A forma de uniões deve ser a mesma entre plataformas para garantir a interconectividade.

Para obter uma descrição da forma de uma União encapsulada, consulte [**Union**](union.md).

## <a name="examples"></a>Exemplos

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

Para obter informações relacionadas, consulte [tipos base de MIDL](midl-base-types.md), [**Char**](char-idl.md), **\[** [**\_ identificador de contexto**](context-handle.md) **\]** , [**enum**](enum.md), **\[** [**primeiro \_ é**](first-is.md) **\]** , **\[** [**identificador**](handle.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** , [**int**](int.md), **\[** [**ignorar**](ignore.md) **\]** , **\[** [**último \_ é**](last-is.md) **\]** , **\[** [**comprimento \_ é**](length-is.md) **\]** , **\[** [**máximo \_ é**](max-is.md), **\]** **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [unencapsulated Unions](nonencapsulated-unions.md), **\[** [**PTR**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**Size \_ is**](size-is.md) **\]** , **\[** [**String**](string.md) **\]** , [**struct**](struct.md), [**switch**](switch.md), **\[** [**switch \_ is**](switch-is.md) **\]** , **\[** [**\_ tipo switch**](switch-type.md) **\]** , **\[** [**Transmit \_ as**](transmit-as.md) **\]** , [**Union**](union.md)e **\[** [**Unique**](unique.md)**\]**

 

 




