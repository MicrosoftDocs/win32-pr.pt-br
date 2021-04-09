---
title: Matrizes de MIDL
description: Matrizes MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- tipos de dados MIDL, matrizes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007493"
---
# <a name="midl-arrays"></a><span data-ttu-id="771df-104">Matrizes de MIDL</span><span class="sxs-lookup"><span data-stu-id="771df-104">MIDL Arrays</span></span>

<span data-ttu-id="771df-105">Os declaradores de matriz aparecem no corpo da interface do arquivo IDL como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="771df-105">Array declarators appear in the interface body of the IDL file as one of the following:</span></span>

-   <span data-ttu-id="771df-106">Parte de uma declaração geral</span><span class="sxs-lookup"><span data-stu-id="771df-106">Part of a general declaration</span></span>
-   <span data-ttu-id="771df-107">Um membro de um Declarador de estrutura ou União</span><span class="sxs-lookup"><span data-stu-id="771df-107">A member of a structure or union declarator</span></span>
-   <span data-ttu-id="771df-108">Um parâmetro para uma chamada de procedimento remoto</span><span class="sxs-lookup"><span data-stu-id="771df-108">A parameter to a remote procedure call</span></span>

<span data-ttu-id="771df-109">Os limites de cada dimensão da matriz são expressos dentro de um par separado de colchetes.</span><span class="sxs-lookup"><span data-stu-id="771df-109">The bounds of each dimension of the array are expressed inside a separate pair of square brackets.</span></span> <span data-ttu-id="771df-110">Uma expressão que é avaliada como *n* significa um limite inferior de zero e um limite superior de *n-1*.</span><span class="sxs-lookup"><span data-stu-id="771df-110">An expression that evaluates to *n* signifies a lower bound of zero and an upper bound of *n - 1*.</span></span> <span data-ttu-id="771df-111">Se os colchetes estiverem vazios ou contiverem um único asterisco ( \* ), o limite inferior será zero e o limite superior será determinado em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="771df-111">If the square brackets are empty or contain a single asterisk (\*), the lower bound is zero and the upper bound is determined at runtime.</span></span>

<span data-ttu-id="771df-112">A matriz também pode conter dois valores separados por uma elipse que representa os limites inferior e superior da matriz, como em \[ *minúsculas*... *superior* \] .</span><span class="sxs-lookup"><span data-stu-id="771df-112">The array can also contain two values separated by an ellipsis that represent the lower and upper bounds of the array, as in \[*lower*...*upper*\].</span></span> <span data-ttu-id="771df-113">O Microsoft RPC requer um limite inferior de zero.</span><span class="sxs-lookup"><span data-stu-id="771df-113">Microsoft RPC requires a lower bound of zero.</span></span> <span data-ttu-id="771df-114">O compilador MIDL não reconhece construções que especificam limites inferiores diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="771df-114">The MIDL compiler does not recognize constructs that specify nonzero lower bounds.</span></span>

<span data-ttu-id="771df-115">As matrizes podem ser associadas com o [**tamanho \_**](size-is.md)dos atributos de campo is, [**Max \_ is**](max-is.md), [**length \_**](length-is.md)is, [**First \_ is**](first-is.md)e [**Last \_ é**](last-is.md) especificar o tamanho da matriz ou a parte da matriz que contém dados válidos.</span><span class="sxs-lookup"><span data-stu-id="771df-115">Arrays can be associated with the field attributes [**size\_is**](size-is.md), [**max\_is**](max-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), and [**last\_is**](last-is.md) to specify the size of the array or the part of the array that contains valid data.</span></span> <span data-ttu-id="771df-116">Esses atributos de campo identificam o parâmetro, o campo de estrutura ou a constante que especifica a dimensão ou o índice da matriz.</span><span class="sxs-lookup"><span data-stu-id="771df-116">These field attributes identify the parameter, structure field, or constant that specifies the array dimension or index.</span></span>

<span data-ttu-id="771df-117">A matriz deve ser associada ao identificador especificado pelo atributo Field da seguinte maneira: quando a matriz é um parâmetro, o identificador também deve ser um parâmetro para a mesma função; Quando a matriz é um campo de estrutura, o identificador deve ser outro campo de estrutura da mesma estrutura.</span><span class="sxs-lookup"><span data-stu-id="771df-117">The array must be associated with the identifier specified by the field attribute in the following way: When the array is a parameter, the identifier must also be a parameter to the same function; when the array is a structure field, the identifier must be another structure field of that same structure.</span></span>

<span data-ttu-id="771df-118">Uma matriz é chamada de "compatível" se o limite superior de qualquer dimensão for determinado em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="771df-118">An array is called "conformant" if the upper bound of any dimension is determined at runtime.</span></span> <span data-ttu-id="771df-119">(Somente os limites superiores podem ser determinados em tempo de execução.) Para determinar o limite superior, a declaração de matriz deve incluir um atributo [**Size \_ is**](size-is.md) ou [**Max \_ is**](max-is.md) .</span><span class="sxs-lookup"><span data-stu-id="771df-119">(Only upper bounds can be determined at runtime.) To determine the upper bound, the array declaration must include a [**size\_is**](size-is.md) or [**max\_is**](max-is.md) attribute.</span></span>

<span data-ttu-id="771df-120">Uma matriz é chamada de "variação" quando seus limites são determinados em tempo de compilação, mas o intervalo de elementos transmitidos é determinado em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="771df-120">An array is called "varying" when its bounds are determined at compile time, but the range of transmitted elements is determined at runtime.</span></span> <span data-ttu-id="771df-121">Para determinar o intervalo de elementos transmitidos, a declaração de matriz deve incluir um comprimento, o [**primeiro \_ é**](first-is.md), ou o [**último \_ é**](last-is.md) o atributo. [**\_**](length-is.md)</span><span class="sxs-lookup"><span data-stu-id="771df-121">To determine the range of transmitted elements, the array declaration must include a [**length\_is**](length-is.md), [**first\_is**](first-is.md), or [**last\_is**](last-is.md) attribute.</span></span>

<span data-ttu-id="771df-122">Uma matriz de variação em conformidade (também chamada de "aberta") é uma matriz cujo limite superior e o intervalo de elementos transmitidos são determinados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="771df-122">A conformant varying array (also called "open") is an array whose upper bound and range of transmitted elements are determined at runtime.</span></span> <span data-ttu-id="771df-123">No máximo, uma matriz de variável compatível ou compatível pode ser aninhada em uma estrutura C e deve ser o último elemento da estrutura.</span><span class="sxs-lookup"><span data-stu-id="771df-123">At most, one conformant or conformant varying array can be nested in a C structure and must be the last element of the structure.</span></span> <span data-ttu-id="771df-124">Por outro lado, matrizes de variação não compatíveis podem ocorrer em qualquer lugar em uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="771df-124">In contrast, nonconformant varying arrays can occur anywhere in a structure.</span></span>

## <a name="examples"></a><span data-ttu-id="771df-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="771df-125">Examples</span></span>

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

<span data-ttu-id="771df-126">Para obter mais informações, consulte [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="771df-126">For more information, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

## <a name="multidimensional-arrays"></a><span data-ttu-id="771df-127">Matrizes multidimensionais</span><span class="sxs-lookup"><span data-stu-id="771df-127">Multidimensional Arrays</span></span>

<span data-ttu-id="771df-128">O usuário pode declarar tipos que são matrizes e, em seguida, declarar matrizes de objetos desses tipos.</span><span class="sxs-lookup"><span data-stu-id="771df-128">The user can declare types that are arrays and then declare arrays of objects of such types.</span></span> <span data-ttu-id="771df-129">A semântica de matrizes *m* bidimensionais de tipos de matriz *n*-dimensional é igual à *semântica de* + matrizes *n*-dimensional.</span><span class="sxs-lookup"><span data-stu-id="771df-129">The semantics of *m*-dimensional arrays of *n*-dimensional array types are the same as the semantics of *m*+*n*-dimensional arrays.</span></span>

<span data-ttu-id="771df-130">Por exemplo, o tipo RECT tipo \_ pode ser definido como uma matriz bidimensional e a variável *Rect* pode ser definida como uma matriz do \_ tipo Rect.</span><span class="sxs-lookup"><span data-stu-id="771df-130">For example, the type RECT\_TYPE can be defined as a two-dimensional array and the variable *rect* can be defined as an array of RECT\_TYPE.</span></span> <span data-ttu-id="771df-131">Isso é equivalente à matriz tridimensional de *\_ retângulo equivalente*:</span><span class="sxs-lookup"><span data-stu-id="771df-131">This is equivalent to the three-dimensional array *equivalent\_rect*:</span></span>

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

<span data-ttu-id="771df-132">O Microsoft RPC é orientado a C.</span><span class="sxs-lookup"><span data-stu-id="771df-132">Microsoft RPC is C oriented.</span></span> <span data-ttu-id="771df-133">Seguindo as convenções de linguagem C, somente a primeira dimensão de uma matriz multidimensional pode ser determinada em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="771df-133">Following C-language conventions, only the first dimension of a multidimensional array can be determined at runtime.</span></span> <span data-ttu-id="771df-134">A interoperação com matrizes de IDL do DCE que dão suporte a outras linguagens é limitada a:</span><span class="sxs-lookup"><span data-stu-id="771df-134">Interoperation with DCE IDL arrays that support other languages is limited to:</span></span>

-   <span data-ttu-id="771df-135">Matrizes multidimensionais com limites constantes (de tempo de compilação).</span><span class="sxs-lookup"><span data-stu-id="771df-135">Multidimensional arrays with constant (compile-time-determined) bounds.</span></span>
-   <span data-ttu-id="771df-136">Matrizes multidimensionais com todos os limites de constante, exceto a primeira dimensão.</span><span class="sxs-lookup"><span data-stu-id="771df-136">Multidimensional arrays with all constant bounds except the first dimension.</span></span> <span data-ttu-id="771df-137">O limite superior e o intervalo de elementos transmitidos da primeira dimensão dependem do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="771df-137">The upper bound and range of transmitted elements of the first dimension are dependent on runtime.</span></span>
-   <span data-ttu-id="771df-138">Qualquer matriz unidimensional com um limite inferior de zero.</span><span class="sxs-lookup"><span data-stu-id="771df-138">Any one-dimensional arrays with a lower bound of zero.</span></span>

<span data-ttu-id="771df-139">Quando o **\[** atributo de [**cadeia de caracteres**](string.md) **\]** é usado em matrizes multidimensionais, o atributo se aplica à matriz mais à direita.</span><span class="sxs-lookup"><span data-stu-id="771df-139">When the **\[**[**string**](string.md)**\]** attribute is used on multidimensional arrays, the attribute applies to the rightmost array.</span></span>

## <a name="arrays-of-pointers"></a><span data-ttu-id="771df-140">Matrizes de ponteiros</span><span class="sxs-lookup"><span data-stu-id="771df-140">Arrays of Pointers</span></span>

<span data-ttu-id="771df-141">Os ponteiros de referência devem apontar para dados válidos.</span><span class="sxs-lookup"><span data-stu-id="771df-141">Reference pointers must point to valid data.</span></span> <span data-ttu-id="771df-142">O aplicativo cliente deve alocar toda a memória para uma **\[** matriz [**in**](in.md) **\]** ou **\[** **in,**[**fora**](out-idl.md) **\]** de ponteiros de referência, especialmente quando a matriz está associada aos valores **\[ in \]**, **\[** **in, out \]**, **\[** [**length \_**](length-is.md) **\]** ou **\[** [**Last \_ is**](last-is.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="771df-142">The client application must allocate all memory for an **\[**[**in**](in.md)**\]** or **\[** **in,**[**out**](out-idl.md)**\]** array of reference pointers, especially when the array is associated with **\[in\]**, or **\[** **in,out\]**, **\[**[**length\_is**](length-is.md)**\]**, or **\[**[**last\_is**](last-is.md)**\]** values.</span></span> <span data-ttu-id="771df-143">O aplicativo cliente também deve inicializar todos os elementos da matriz antes da chamada.</span><span class="sxs-lookup"><span data-stu-id="771df-143">The client application must also initialize all array elements before the call.</span></span> <span data-ttu-id="771df-144">Antes de retornar ao cliente, o aplicativo de servidor deve verificar se todos os elementos de matriz no intervalo transmitido apontam para um armazenamento válido.</span><span class="sxs-lookup"><span data-stu-id="771df-144">Before returning to the client, the server application must verify that all array elements in the transmitted range point to valid storage.</span></span>

<span data-ttu-id="771df-145">No lado do servidor, o stub aloca armazenamento para todos os elementos da matriz, independentemente do **\[** [**comprimento \_**](length-is.md) **\]** ou do **\[** [**último \_**](last-is.md) **\]** valor no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="771df-145">On the server side, the stub allocates storage for all array elements, regardless of the **\[**[**length\_is**](length-is.md)**\]** or **\[**[**last\_is**](last-is.md)**\]** value at the time of the call.</span></span> <span data-ttu-id="771df-146">Esse recurso pode afetar o desempenho do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="771df-146">This feature can affect the performance of your application.</span></span>

<span data-ttu-id="771df-147">Nenhuma restrição é colocada em matrizes de ponteiros exclusivos.</span><span class="sxs-lookup"><span data-stu-id="771df-147">No restrictions are placed on arrays of unique pointers.</span></span> <span data-ttu-id="771df-148">No cliente e no servidor, o armazenamento é alocado para ponteiros nulos.</span><span class="sxs-lookup"><span data-stu-id="771df-148">On both the client and the server, storage is allocated for null pointers.</span></span> <span data-ttu-id="771df-149">Quando os ponteiros são não nulos, os dados são colocados no armazenamento pré-alocado.</span><span class="sxs-lookup"><span data-stu-id="771df-149">When pointers are non-null, data is placed in preallocated storage.</span></span>

<span data-ttu-id="771df-150">Um Declarador de ponteiro opcional pode preceder o Declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="771df-150">An optional pointer declarator can precede the array declarator.</span></span>

<span data-ttu-id="771df-151">Quando ponteiros de referência inseridos são **\[** [](out-idl.md) **\]** parâmetros somente out, o código do Gerenciador de servidores deve atribuir valores válidos à matriz de ponteiros de referência.</span><span class="sxs-lookup"><span data-stu-id="771df-151">When embedded reference pointers are **\[**[**out**](out-idl.md)**\]**-only parameters, the server-manager code must assign valid values to the array of reference pointers.</span></span> <span data-ttu-id="771df-152">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="771df-152">For example:</span></span>

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

<span data-ttu-id="771df-153">Os stubs gerados alocam a matriz e atribuem valores nulos a todos os ponteiros inseridos na matriz.</span><span class="sxs-lookup"><span data-stu-id="771df-153">The generated stubs allocate the array and assign null values to all pointers embedded in the array.</span></span>

 

 