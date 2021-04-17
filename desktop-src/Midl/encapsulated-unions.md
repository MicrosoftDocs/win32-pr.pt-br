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
# <a name="encapsulated-unions"></a><span data-ttu-id="369b4-104">Uniões encapsuladas</span><span class="sxs-lookup"><span data-stu-id="369b4-104">Encapsulated Unions</span></span>

<span data-ttu-id="369b4-105">Uma União que está contida com seu discriminante em uma estrutura dentro do é uma União encapsulada.</span><span class="sxs-lookup"><span data-stu-id="369b4-105">A union that is contained with its discriminant in a structure within is an encapsulated union.</span></span> <span data-ttu-id="369b4-106">A União encapsulada é indicada pela presença da palavra-chave [**switch**](switch.md) .</span><span class="sxs-lookup"><span data-stu-id="369b4-106">The encapsulated union is indicated by the presence of the [**switch**](switch.md) keyword.</span></span> <span data-ttu-id="369b4-107">Esse tipo de União é tão nomeado porque o compilador MIDL encapsula automaticamente a União e seu discriminante em uma estrutura para transmissão durante uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="369b4-107">This type of union is so named because the MIDL compiler automatically encapsulates the union and its discriminant in a structure for transmission during a remote procedure call.</span></span>

<span data-ttu-id="369b4-108">Se a marca Union estiver ausente (U1 \_ Type no exemplo acima), o compilador irá gerar a estrutura com o campo Union chamado *\_ Union marcada*.</span><span class="sxs-lookup"><span data-stu-id="369b4-108">If the union tag is missing (U1\_TYPE in the example above), the compiler will generate the structure with the union field named *tagged\_union*.</span></span>

<span data-ttu-id="369b4-109">A forma de uniões deve ser a mesma entre plataformas para garantir a interconectividade.</span><span class="sxs-lookup"><span data-stu-id="369b4-109">The shape of unions must be the same across platforms to ensure interconnectivity.</span></span>

<span data-ttu-id="369b4-110">Para obter uma descrição da forma de uma União encapsulada, consulte [**Union**](union.md).</span><span class="sxs-lookup"><span data-stu-id="369b4-110">For a description of the form of an encapsulated union, see [**union**](union.md).</span></span>

## <a name="examples"></a><span data-ttu-id="369b4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="369b4-111">Examples</span></span>

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

<span data-ttu-id="369b4-112">Para obter informações relacionadas, consulte [tipos base de MIDL](midl-base-types.md), [**Char**](char-idl.md), **\[** [**\_ identificador de contexto**](context-handle.md) **\]** , [**enum**](enum.md), **\[** [**primeiro \_ é**](first-is.md) **\]** , **\[** [**identificador**](handle.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** , [**int**](int.md), **\[** [**ignorar**](ignore.md) **\]** , **\[** [**último \_ é**](last-is.md) **\]** , **\[** [**comprimento \_ é**](length-is.md) **\]** , **\[** [**máximo \_ é**](max-is.md), **\]** **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [unencapsulated Unions](nonencapsulated-unions.md), **\[** [**PTR**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**Size \_ is**](size-is.md) **\]** , **\[** [**String**](string.md) **\]** , [**struct**](struct.md), [**switch**](switch.md), **\[** [**switch \_ is**](switch-is.md) **\]** , **\[** [**\_ tipo switch**](switch-type.md) **\]** , **\[** [**Transmit \_ as**](transmit-as.md) **\]** , [**Union**](union.md)e **\[** [**Unique**](unique.md)**\]**</span><span class="sxs-lookup"><span data-stu-id="369b4-112">For related information, see [MIDL Base Types](midl-base-types.md), [**char**](char-idl.md), **\[**[**context\_handle**](context-handle.md)**\]**, [**enum**](enum.md), **\[**[**first\_is**](first-is.md)**\]**, **\[**[**handle**](handle.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, [**int**](int.md), **\[**[**ignore**](ignore.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**ms\_union**](ms-union-attrib.md)**\]**, [Nonencapsulated Unions](nonencapsulated-unions.md), **\[**[**ptr**](ptr.md)**\]**, **\[**[**ref**](ref.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, **\[**[**string**](string.md)**\]**, [**struct**](struct.md), [**switch**](switch.md), **\[**[**switch\_is**](switch-is.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**, [**union**](union.md), and **\[**[**unique**](unique.md)**\]**</span></span>

 

 




