---
title: Indicadores de tipo
description: As propriedades reais seguem a tabela de valores do conjunto de propriedades de identificadores de propriedade/pares de deslocamento. Cada propriedade é armazenada como uma DWORD, seguida pelo valor do tipo de dados.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007909"
---
# <a name="type-indicators"></a><span data-ttu-id="c333c-104">Indicadores de tipo</span><span class="sxs-lookup"><span data-stu-id="c333c-104">Type Indicators</span></span>

<span data-ttu-id="c333c-105">As propriedades reais seguem a tabela de valores do conjunto de propriedades de identificadores de propriedade/pares de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="c333c-105">The actual properties follow the table of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="c333c-106">Cada propriedade é armazenada como uma **DWORD**, seguida pelo valor do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c333c-106">Each property is stored as a **DWORD**, followed by the data type value.</span></span>

<span data-ttu-id="c333c-107">Os indicadores de tipo e seus valores associados são descritos na estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="c333c-107">Type indicators and their associated values are described in the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="c333c-108">Todos os pares de tipo/valor devem começar em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c333c-108">All Type/Value pairs must begin on a 32-bit boundary.</span></span> <span data-ttu-id="c333c-109">Assim, os valores podem ser seguidos com bytes nulos para alinhar o par subsequente em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c333c-109">Thus, values may be followed with null bytes to align the subsequent pair on a 32-bit boundary.</span></span>

<span data-ttu-id="c333c-110">O código de exemplo a seguir calcula quantos bytes são necessários para alinhar em um limite de 32 bits, dada uma contagem de bytes.</span><span class="sxs-lookup"><span data-stu-id="c333c-110">The following example code calculates how many bytes are required to align on a 32-bit boundary, given a count of bytes.</span></span>


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



<span data-ttu-id="c333c-111">Dentro de um vetor de valores, cada repetição de um valor escalar simples menor que 32 bits deve ser alinhada com seu alinhamento natural, e não com um alinhamento de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c333c-111">Within a vector of values, each repetition of a simple scalar value smaller than 32 bits must align with its natural alignment rather than with a 32-bit alignment.</span></span> <span data-ttu-id="c333c-112">Na prática, isso só é significativo para os **tipos \_ VT UI1**, **VT \_ UI2**, **VT \_ i2** e **VT \_ bool** (que têm alinhamento natural de um ou dois bytes).</span><span class="sxs-lookup"><span data-stu-id="c333c-112">In practice, this is only significant for types **VT\_UI1**, **VT\_UI2**, **VT\_I2**, and **VT\_BOOL** (which have one-byte or two-byte natural alignment).</span></span> <span data-ttu-id="c333c-113">Todos os outros tipos têm alinhamento natural de quatro bytes.</span><span class="sxs-lookup"><span data-stu-id="c333c-113">All other types have four-byte natural alignment.</span></span> <span data-ttu-id="c333c-114">Alguns tipos, por exemplo, **a \_ R8 de VT**, na verdade têm um alinhamento natural de 8 bytes, mas são armazenados como se tivessem um alinhamento de quatro bytes.</span><span class="sxs-lookup"><span data-stu-id="c333c-114">Some types, for example, **VT\_R8**, actually have 8-byte natural alignment, but are stored as if they have four-byte alignment.</span></span>

<span data-ttu-id="c333c-115">Um valor de propriedade com o símbolo de tipo **VT \_ i2** \| **VT \_ vector** incluiria:</span><span class="sxs-lookup"><span data-stu-id="c333c-115">A property value with type indicator **VT\_I2** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="c333c-116">Uma contagem de elementos **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c333c-116">A **DWORD** element count.</span></span>
-   <span data-ttu-id="c333c-117">Uma sequência de inteiros de dois bytes empacotados sem nenhum preenchimento nulo entre eles.</span><span class="sxs-lookup"><span data-stu-id="c333c-117">A sequence of packed two-byte integers with no null padding between them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c333c-118">Quaisquer contagens de 32 bits ou tipos de propriedade que são armazenados como parte de um elemento de propriedade de vetor também devem ser alinhados em 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c333c-118">Any 32-bit counts or property types that are stored as a part of a vector property element must also be 32-bit aligned.</span></span>

 

<span data-ttu-id="c333c-119">Um valor de Propriedade do tipo identificador **VT \_ LPSTR** do \| **\_ vetor VT** incluiria:</span><span class="sxs-lookup"><span data-stu-id="c333c-119">A property value of type identifier **VT\_LPSTR** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="c333c-120">Uma contagem de elementos **DWORD** (**DWORD** *cElems*).</span><span class="sxs-lookup"><span data-stu-id="c333c-120">A **DWORD** element count (**DWORD** *cElems*).</span></span>
-   <span data-ttu-id="c333c-121">Uma sequência de cadeias de caracteres (**Char** *rgch \[ \]*), cada uma precedida por um **DWORD** de contagem de comprimento e possivelmente seguida por um preenchimento nulo para arredondar para um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c333c-121">A sequence of strings (**char** *rgch\[\]*), each preceded by a length-count **DWORD** and possibly followed by null padding to round to a 32-bit boundary.</span></span>

 

 