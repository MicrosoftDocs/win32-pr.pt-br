---
title: Matrizes multidimensionais
description: Os atributos de matriz também podem ser usados com matrizes multidimensionais.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917522"
---
# <a name="multidimensional-arrays"></a><span data-ttu-id="cc7d5-103">Matrizes multidimensionais</span><span class="sxs-lookup"><span data-stu-id="cc7d5-103">Multidimensional Arrays</span></span>

<span data-ttu-id="cc7d5-104">Os atributos de matriz também podem ser usados com matrizes multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-104">Array attributes can also be used with multidimensional arrays.</span></span> <span data-ttu-id="cc7d5-105">No entanto, tenha cuidado para garantir que cada dimensão da matriz tenha um atributo correspondente.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-105">However, be careful to ensure that every dimension of the array has a corresponding attribute.</span></span> <span data-ttu-id="cc7d5-106">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-106">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

<span data-ttu-id="cc7d5-107">A matriz anterior é uma matriz compatível (de tamanho d1size) de 30 matrizes de elementos (com elementos d2len enviados para cada um).</span><span class="sxs-lookup"><span data-stu-id="cc7d5-107">The preceding array is a conformant array (of size d1size ) of 30 element arrays (with d2len elements shipped for each).</span></span> <span data-ttu-id="cc7d5-108">A vírgula entre parênteses do \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is) o \] atributo especifica que o valor em d1size é aplicado à primeira dimensão da matriz.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-108">The comma in the parentheses of the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute specifies that value in d1size is applied to the first dimension of the array.</span></span> <span data-ttu-id="cc7d5-109">Da mesma forma, o comando nos parênteses de \[ [**length \_ é**](/windows/desktop/Midl/length-is) o \] atributo indica que o valor em d2len é aplicado à segunda dimensão da matriz.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-109">Likewise, the command in the parentheses of the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute indicates that the value in d2len is applied to the second dimension of the array.</span></span>

<span data-ttu-id="cc7d5-110">O compilador MIDL 2,0 fornece dois métodos de marshaling de parâmetros: modo misto (/**os**) e totalmente interpretado (/**OIF** ou/**Oicf**).</span><span class="sxs-lookup"><span data-stu-id="cc7d5-110">The MIDL 2.0 compiler provides two methods for marshaling parameters: mixed-mode (/**Os**) and fully-interpreted (/**Oif** or /**Oicf**).</span></span> <span data-ttu-id="cc7d5-111">Por padrão, o compilador MIDL compila interfaces no modo misto.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-111">By default, the MIDL compiler compiles interfaces in mixed mode.</span></span> <span data-ttu-id="cc7d5-112">Você não precisa especificar explicitamente a opção [**/os**](/windows/desktop/Midl/-os) para obter marshaling de modo misto.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-112">You do not need to explicitly specify the [**/Os**](/windows/desktop/Midl/-os) switch to get mixed-mode marshaling.</span></span>

<span data-ttu-id="cc7d5-113">O método totalmente interpretado realiza marshaling de dados completamente offline.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-113">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="cc7d5-114">Isso reduz consideravelmente o tamanho do código stub, mas também resulta em desempenho reduzido.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-114">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span> <span data-ttu-id="cc7d5-115">No marshaling de modo misto, os stubs realiza marshaling de alguns parâmetros online.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-115">In mixed-mode marshaling, the stubs marshals some parameters online.</span></span> <span data-ttu-id="cc7d5-116">Embora isso resulte em um tamanho maior de stub, ele também oferece maior desempenho.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-116">While this results in a larger stub size, it also offers increased performance.</span></span>

> [!Caution]  
> <span data-ttu-id="cc7d5-117">Tenha cuidado ao compilar arquivos IDL nesse modo.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-117">Exercise caution when compiling IDL files in this mode.</span></span> <span data-ttu-id="cc7d5-118">O uso de matrizes multidimensionais no modo misto pode resultar em parâmetros que não são empacotados corretamente.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-118">Using multidimensional arrays in mixed mode can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="cc7d5-119">A opção de linha de comando [**/Oicf**](/windows/desktop/Midl/-oi) é recomendada quando sua interface define parâmetros que são matrizes multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-119">The [**/Oicf**](/windows/desktop/Midl/-oi) command line switch is recommended when your interface defines parameters that are multidimensional arrays.</span></span>

 

<span data-ttu-id="cc7d5-120">O \[ atributo de [**cadeia de caracteres**](/windows/desktop/Midl/string) \] também pode ser usado com matrizes multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-120">The \[[**string**](/windows/desktop/Midl/string)\] attribute can also be used with multidimensional arrays.</span></span> <span data-ttu-id="cc7d5-121">O atributo aplica-se à dimensão menos significativa, como uma matriz de cadeias de caracteres compatível.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-121">The attribute applies to the least significant dimension, such as a conformant array of strings.</span></span> <span data-ttu-id="cc7d5-122">Você também pode usar atributos de ponteiro multidimensional.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-122">You can also use multidimensional pointer attributes.</span></span> <span data-ttu-id="cc7d5-123">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-123">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

<span data-ttu-id="cc7d5-124">No exemplo anterior, a variável ptr2d é um ponteiro para um bloco de ponteiros de tamanho d1len, cada um dos quais aponta para d2len ponteiros para **Long**.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-124">In the preceding example, the variable ptr2d is a pointer to a d1len-sized block of pointers, each of which points to d2len pointers to **long**.</span></span>

<span data-ttu-id="cc7d5-125">Matrizes multidimensionais não são equivalentes a matrizes de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-125">Multidimensional arrays are not equivalent to arrays of pointers.</span></span> <span data-ttu-id="cc7d5-126">Uma matriz multidimensional é um bloco de dados único e grande na memória.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-126">A multidimensional array is a single, large block of data in memory.</span></span> <span data-ttu-id="cc7d5-127">Uma matriz de ponteiros contém apenas um bloco de ponteiros na matriz.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-127">An array of pointers only contains a block of pointers in the array.</span></span> <span data-ttu-id="cc7d5-128">Os dados aos quais os ponteiros apontam podem estar em qualquer lugar na memória.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-128">The data that the pointers point to can be anywhere in memory.</span></span> <span data-ttu-id="cc7d5-129">Além disso, a sintaxe ANSI C permite que apenas a dimensão de matriz mais significativa (mais à esquerda) não seja especificada em uma matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="cc7d5-129">Also, ANSI C syntax allows only the most significant (leftmost) array dimension to be unspecified in a multidimensional array.</span></span> <span data-ttu-id="cc7d5-130">Portanto, a seguir está uma instrução válida:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-130">Therefore, the following is a valid statement:</span></span>

`long a1[] [20]`

<span data-ttu-id="cc7d5-131">Compare isso com a seguinte instrução inválida:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-131">Compare this to the following invalid statement:</span></span>

`long a1[20] []`

 

 