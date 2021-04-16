---
description: Um tipo portátil usado para representar um vetor de ponto flutuante de 4 32 bits ou componentes inteiros, cada um alinhado de forma ideal e mapeado para um registro de vetor de hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo de dados XMVECTOR (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765673"
---
# <a name="xmvector-data-type"></a><span data-ttu-id="6808a-103">Tipo de dados XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="6808a-103">XMVECTOR Data Type</span></span>

<span data-ttu-id="6808a-104">Um tipo portátil usado para representar um vetor de ponto flutuante de 4 32 bits ou componentes inteiros, cada um alinhado de forma ideal e mapeado para um registro de vetor de hardware.</span><span class="sxs-lookup"><span data-stu-id="6808a-104">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6808a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6808a-105">Remarks</span></span>

<span data-ttu-id="6808a-106">Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis usando `XMVECTOR` ao programar em C++, consulte [extensões de XMVECTOR](ovw-xmvector-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="6808a-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTOR` when programming in C++, see [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span></span>

<span data-ttu-id="6808a-107">Na biblioteca DirectXMath, para dar suporte total à portabilidade e otimização, `XMVECTOR` é, por design, um tipo opaco.</span><span class="sxs-lookup"><span data-stu-id="6808a-107">In the DirectXMath Library, to fully support portability and optimization, `XMVECTOR` is, by design, an opaque type.</span></span> <span data-ttu-id="6808a-108">A implementação real do `XMVECTOR` é dependente da plataforma.</span><span class="sxs-lookup"><span data-stu-id="6808a-108">The actual implementation of `XMVECTOR` is platform dependent.</span></span>

<span data-ttu-id="6808a-109">Em geral, o código não deve contar com as especificidades de uma determinada implementação específica da plataforma do `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="6808a-109">In general, code should not rely on the specifics of any given platform specific implementation of `XMVECTOR`.</span></span> <span data-ttu-id="6808a-110">Implementações específicas da plataforma têm estas características:</span><span class="sxs-lookup"><span data-stu-id="6808a-110">Platform-specific implementations have these characteristics:</span></span>

-   <span data-ttu-id="6808a-111">Eles não são portáteis.</span><span class="sxs-lookup"><span data-stu-id="6808a-111">They are not portable.</span></span>
-   <span data-ttu-id="6808a-112">Eles podem ser alterados entre as versões.</span><span class="sxs-lookup"><span data-stu-id="6808a-112">They may change between releases.</span></span>
-   <span data-ttu-id="6808a-113">O uso incriterioso de detalhes de implementação pode ser inferior.</span><span class="sxs-lookup"><span data-stu-id="6808a-113">Injudicious use of implementation details may be suboptimal.</span></span>

<span data-ttu-id="6808a-114">Os desenvolvedores devem usar as funções [acessador](ovw-xnamath-reference-functions-accessors.md), [carga](ovw-xnamath-reference-functions-load.md)e [armazenamento](ovw-xnamath-reference-functions-storage.md) da biblioteca DirectXMath para obter e definir os vetores e as [funções de vetor 4D da biblioteca DirectXMath](ovw-xnamath-reference-functions-vector4.md) para manipulá-los.</span><span class="sxs-lookup"><span data-stu-id="6808a-114">Developers should use DirectXMath Library's [accessor](ovw-xnamath-reference-functions-accessors.md), [load](ovw-xnamath-reference-functions-load.md), and [store](ovw-xnamath-reference-functions-storage.md) functions to get and set the vectors, and the [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) to manipulate them.</span></span>

<span data-ttu-id="6808a-115">Para projetos que precisam de informações detalhadas sobre como implementar `XMVECTOR` em diferentes plataformas, consulte [elementos internos da biblioteca](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="6808a-115">For projects that need detailed information about how to implement `XMVECTOR` on different platforms, see [Library Internals](pg-xnamath-internals.md).</span></span>

### <a name="compiler-aliases"></a><span data-ttu-id="6808a-116">Aliases do compilador</span><span class="sxs-lookup"><span data-stu-id="6808a-116">Compiler Aliases</span></span>

<span data-ttu-id="6808a-117">O arquivo de cabeçalho DirectXMath. h usa aliases para o `XMVECTOR` objeto, especificamente **CXMVECTOR** e **FXMVECTOR**.</span><span class="sxs-lookup"><span data-stu-id="6808a-117">The DirectXMath.h header file uses aliases to the `XMVECTOR` object, specifically **CXMVECTOR** and **FXMVECTOR**.</span></span> <span data-ttu-id="6808a-118">O cabeçalho usa esses aliases para obedecer às convenções de chamada internas ideais de compiladores diferentes.</span><span class="sxs-lookup"><span data-stu-id="6808a-118">The header uses these aliases to comply with the optimal in-line calling conventions of different compilers.</span></span> <span data-ttu-id="6808a-119">Para a maioria dos projetos que usam DirectXMath, é suficiente tratar esses tipos como um alias exato para `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="6808a-119">For most projects that use DirectXMath it is sufficient to treat these types as an exact alias to `XMVECTOR`.</span></span>

<span data-ttu-id="6808a-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6808a-120">For example:</span></span>


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



<span data-ttu-id="6808a-121">Para projetos que precisam de informações detalhadas sobre como diferentes plataformas manipulam suas convenções de chamada, consulte [elementos internos da biblioteca](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="6808a-121">For projects that need detailed information about how different platforms handle their calling conventions, see [Library Internals](pg-xnamath-internals.md).</span></span>

<span data-ttu-id="6808a-122">Para XNAMATH 2. x, o `XMVECTOR` tipo de dados tem os membros do elemento. x,. y,. z,. e. w, o que geralmente causa baixo desempenho.</span><span class="sxs-lookup"><span data-stu-id="6808a-122">For XNAMATH 2.x, the `XMVECTOR` data type has .x, .y, .z, .and .w element members, which generally cause poor performance.</span></span> <span data-ttu-id="6808a-123">O uso do tipo XM \_ estrito \_ VECTOR4 fornece uma aceitação da definição de DirectXMath de um tipo de dados opaco.</span><span class="sxs-lookup"><span data-stu-id="6808a-123">The use of the XM\_STRICT\_VECTOR4 type provides an opt-in of the DirectXMath definition of an opaque data type.</span></span>

<span data-ttu-id="6808a-124">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="6808a-124">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="6808a-125">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="6808a-125">Platform Requirements</span></span>

<span data-ttu-id="6808a-126">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6808a-126">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="6808a-127">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="6808a-127">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="6808a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6808a-128">Requirements</span></span>



| <span data-ttu-id="6808a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6808a-129">Requirement</span></span> | <span data-ttu-id="6808a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6808a-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6808a-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6808a-131">Header</span></span><br/> | <dl> <span data-ttu-id="6808a-132"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="6808a-132"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6808a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6808a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6808a-134">Tipos de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="6808a-134">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="6808a-135">**Tipo de dados XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="6808a-135">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="6808a-136">**Tipo de dados XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="6808a-136">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="6808a-137">**Tipo de dados XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="6808a-137">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="6808a-138">**Tipo de dados XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="6808a-138">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="6808a-139">**Tipo de dados XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="6808a-139">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 




