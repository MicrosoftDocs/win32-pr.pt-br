---
description: Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática XNA para a biblioteca DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migração de código da Biblioteca matemática XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549958"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="996e5-103">Migração de código da Biblioteca matemática XNA</span><span class="sxs-lookup"><span data-stu-id="996e5-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="996e5-104">Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática XNA para a biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="996e5-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

## <a name="header-changes"></a><span data-ttu-id="996e5-105">Alterações de cabeça</span><span class="sxs-lookup"><span data-stu-id="996e5-105">Header Changes</span></span>

<span data-ttu-id="996e5-106">A biblioteca DirectXMath usa um novo conjunto de headers.</span><span class="sxs-lookup"><span data-stu-id="996e5-106">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="996e5-107">Substitua o `xnamath.h` título por e adicione para os tipos `DirectXMath.h` `DirectXPackedVector.h` *empacotados por GPU.*</span><span class="sxs-lookup"><span data-stu-id="996e5-107">Replace the `xnamath.h` header with `DirectXMath.h`, and add `DirectXPackedVector.h` for the *GPU packed* types.</span></span>

<span data-ttu-id="996e5-108">Os tipos delimitativos do exemplo de Colisão do SDK do DirectX no agora fazem parte `xnacollision.h` da biblioteca DirectXMath no `DirectXCollision.h` .</span><span class="sxs-lookup"><span data-stu-id="996e5-108">The bounding types from the DirectX SDK Collision sample in `xnacollision.h` is now part of the DirectXMath library in `DirectXCollision.h`.</span></span> <span data-ttu-id="996e5-109">Eles foram modificados para usar classes C++ em vez de uma API no estilo C.</span><span class="sxs-lookup"><span data-stu-id="996e5-109">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="996e5-110">Alterações constantes</span><span class="sxs-lookup"><span data-stu-id="996e5-110">Constant Changes</span></span>

<span data-ttu-id="996e5-111">A VERSÃO XNAMATH \_ (200, 201, 202, 203, 204 e assim por diante) foi substituída pela VERSÃO DIRECXTMATH \_ (300, 301, 302, 303 e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="996e5-111">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!NOTE]  
> <span data-ttu-id="996e5-112">DirectXMath 3.00 e 3.02 fornecidos com versões preliminares do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="996e5-112">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="996e5-113">O DirectXMath 3.03 está na versão final do SDK do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="996e5-113">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

## <a name="namespaces"></a><span data-ttu-id="996e5-114">Namespaces</span><span class="sxs-lookup"><span data-stu-id="996e5-114">Namespaces</span></span>

<span data-ttu-id="996e5-115">A biblioteca DirectXMath usa namespaces C++ para organizar os tipos.</span><span class="sxs-lookup"><span data-stu-id="996e5-115">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="996e5-116">A Matemática XNA usou apenas o namespace global.</span><span class="sxs-lookup"><span data-stu-id="996e5-116">XNA Math used only the global namespace.</span></span> <span data-ttu-id="996e5-117">Os tipos DirectXMath em comum com a Matemática XNA estão no namespace **DirectX** **ou directX::P ackedVector.**</span><span class="sxs-lookup"><span data-stu-id="996e5-117">The DirectXMath types in common with XNA Math are in the **DirectX** or the **DirectX::PackedVector** namespace.</span></span>

<span data-ttu-id="996e5-118">Em arquivos de origem do C++, uma solução simples é adicionar `using` instruções.</span><span class="sxs-lookup"><span data-stu-id="996e5-118">In C++ source files, a simple solution is to add `using` statements.</span></span>

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

<span data-ttu-id="996e5-119">Para os headers, não é considerada uma melhor prática adicionar instruções using.</span><span class="sxs-lookup"><span data-stu-id="996e5-119">For headers, it is not considered best practice to add using statements.</span></span> <span data-ttu-id="996e5-120">Em vez disso, adicione namespaces totalmente qualificados.</span><span class="sxs-lookup"><span data-stu-id="996e5-120">Instead, add fully-qualified namespaces.</span></span>

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a><span data-ttu-id="996e5-121">Cargas parciais</span><span class="sxs-lookup"><span data-stu-id="996e5-121">Partial Loads</span></span>

<span data-ttu-id="996e5-122">Para várias funções que carregam menos de 4 elementos de um XMVECTOR, a biblioteca matemática XNA deixou os elementos adicionais indefinido.</span><span class="sxs-lookup"><span data-stu-id="996e5-122">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="996e5-123">DirectXMath sempre preencherá esses elementos adicionais com 0.</span><span class="sxs-lookup"><span data-stu-id="996e5-123">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="996e5-124">Remoção de Xbox 360 tipos específicos</span><span class="sxs-lookup"><span data-stu-id="996e5-124">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="996e5-125">Os seguintes tipos, funções e constantes da biblioteca matemática XNA não estão disponíveis no DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="996e5-125">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="996e5-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="996e5-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="996e5-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="996e5-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="996e5-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="996e5-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="996e5-129">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="996e5-129">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="996e5-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="996e5-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="996e5-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="996e5-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="996e5-132">XMStoreXIcoN4(), XMStoreXIco4(), XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="996e5-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="996e5-133">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="996e5-133">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="996e5-134">\_\_vector4i foi preterido.</span><span class="sxs-lookup"><span data-stu-id="996e5-134">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="996e5-135">Em vez disso, use [**XMVECTORI32**](xmvectori32-data-type.md) [**ou XMVECTORU32.**](xmvectoru32-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="996e5-135">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="996e5-136">As seguintes funções e tipos são preterido porque são somente Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="996e5-136">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="996e5-137">Intrínsecos arm-NEON</span><span class="sxs-lookup"><span data-stu-id="996e5-137">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="996e5-138">Declarar uma constante de vetor com esse código será compilado para Matemática XNA para SSE e NO-INTRINSICS, mas falhará para DirectXMath usando ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="996e5-138">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

<span data-ttu-id="996e5-139">Em geral, não recomendamos esse método de inicialização de um [**XMVECTOR.**](xmvector-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="996e5-139">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="996e5-140">No entanto, se você quiser uma constante de vetor, a classe [**XMVECTORF32**](xmvectorf32-data-type.md) dá suporte a esse estilo de inicialização e retorna o tipo **XMVECTOR** automaticamente para que você possa usar **XMVECTORF32** na maioria dos mesmos contextos.</span><span class="sxs-lookup"><span data-stu-id="996e5-140">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="996e5-141">Todas as operações de gravação em **uma classe XMVECTORF32** exigem referenciar explicitamente o membro **XMVECTOR** .v.</span><span class="sxs-lookup"><span data-stu-id="996e5-141">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="996e5-142">Permutar</span><span class="sxs-lookup"><span data-stu-id="996e5-142">Permute</span></span>

<span data-ttu-id="996e5-143">A biblioteca matemática XNA tinha o seguinte formulário para o permute de vetor geral:</span><span class="sxs-lookup"><span data-stu-id="996e5-143">The XNA Math library had the following form for general vector permute:</span></span>

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

<span data-ttu-id="996e5-144">Para DirectXMath, **XMVectorPermuteControl** foi eliminado e o XM \_ PERMUTE \_ 0X ..</span><span class="sxs-lookup"><span data-stu-id="996e5-144">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="996e5-145">As \_ constantes XM PERMUTE 1Z foram redefinidas para serem índices simples \_ de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="996e5-145">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="996e5-146">Aqui está a nova assinatura para [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)</span><span class="sxs-lookup"><span data-stu-id="996e5-146">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

<span data-ttu-id="996e5-147">Em vez de uma palavra de controle, essa função usa diretamente os quatro índices como parâmetros, o que também a torna análoga à função [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) usando o novo XM \_ SWIZZLE \_ X .</span><span class="sxs-lookup"><span data-stu-id="996e5-147">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="996e5-148">Constantes SWIZZLE W XM definidas como índices simples de \_ \_ 0 a 3.</span><span class="sxs-lookup"><span data-stu-id="996e5-148">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> <span data-ttu-id="996e5-149">Para valores constantes, há uma maneira muito mais eficiente de implementar o permute.</span><span class="sxs-lookup"><span data-stu-id="996e5-149">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="996e5-150">Em vez de usar a forma de função [**de XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use o **formulário de** modelo:</span><span class="sxs-lookup"><span data-stu-id="996e5-150">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a><span data-ttu-id="996e5-151">Formulários de modelo</span><span class="sxs-lookup"><span data-stu-id="996e5-151">Template Forms</span></span>

<span data-ttu-id="996e5-152">Em geral, o uso de um formulário de modelo em uma forma de função das funções a seguir é muito mais eficiente e permite que a biblioteca faça otimizações específicas da plataforma por meio da especialização de modelo.</span><span class="sxs-lookup"><span data-stu-id="996e5-152">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a><span data-ttu-id="996e5-153">Funções eliminadas</span><span class="sxs-lookup"><span data-stu-id="996e5-153">Eliminated Functions</span></span>

| <span data-ttu-id="996e5-154">Função eliminada</span><span class="sxs-lookup"><span data-stu-id="996e5-154">Eliminated Function</span></span>        | <span data-ttu-id="996e5-155">Substituição</span><span class="sxs-lookup"><span data-stu-id="996e5-155">Replacement</span></span>                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996e5-156">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="996e5-156">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="996e5-157">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="996e5-157">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| <span data-ttu-id="996e5-158">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="996e5-158">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="996e5-159">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="996e5-159">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| <span data-ttu-id="996e5-160">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="996e5-160">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="996e5-161">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="996e5-161">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| <span data-ttu-id="996e5-162">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="996e5-162">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="996e5-163">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="996e5-163">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| <span data-ttu-id="996e5-164">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="996e5-164">XMStoreInt4NC</span></span>              | [<span data-ttu-id="996e5-165">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="996e5-165">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| <span data-ttu-id="996e5-166">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="996e5-166">XMVector2InBoundsR</span></span>         | <span data-ttu-id="996e5-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="996e5-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="996e5-168">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="996e5-168">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="996e5-169">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="996e5-169">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="996e5-170">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="996e5-170">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| <span data-ttu-id="996e5-171">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="996e5-171">XMVector3InBoundsR</span></span>         | <span data-ttu-id="996e5-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="996e5-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="996e5-173">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="996e5-173">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="996e5-174">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="996e5-174">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="996e5-175">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="996e5-175">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| <span data-ttu-id="996e5-176">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="996e5-176">XMVector4InBoundsR</span></span>         | <span data-ttu-id="996e5-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="996e5-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="996e5-178">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="996e5-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="996e5-179">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="996e5-179">XMVectorCosHEst</span></span>            | [<span data-ttu-id="996e5-180">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="996e5-180">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| <span data-ttu-id="996e5-181">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="996e5-181">XMVectorExpEst</span></span>             | [<span data-ttu-id="996e5-182">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="996e5-182">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| <span data-ttu-id="996e5-183">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="996e5-183">XMVectorLogEst</span></span>             | [<span data-ttu-id="996e5-184">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="996e5-184">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| <span data-ttu-id="996e5-185">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="996e5-185">XMVectorPowEst</span></span>             | [<span data-ttu-id="996e5-186">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="996e5-186">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| <span data-ttu-id="996e5-187">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="996e5-187">XMVectorSinHEst</span></span>            | [<span data-ttu-id="996e5-188">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="996e5-188">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| <span data-ttu-id="996e5-189">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="996e5-189">XMVectorTanHEst</span></span>            | [<span data-ttu-id="996e5-190">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="996e5-190">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a><span data-ttu-id="996e5-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="996e5-191">Related topics</span></span>

[<span data-ttu-id="996e5-192">Guia de Programação do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="996e5-192">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
