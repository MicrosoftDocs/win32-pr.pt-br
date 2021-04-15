---
description: Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática do XNA para a biblioteca DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migração de código da biblioteca de matemática do XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502318"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="2fd70-103">Migração de código da biblioteca de matemática do XNA</span><span class="sxs-lookup"><span data-stu-id="2fd70-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="2fd70-104">Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática do XNA para a biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="2fd70-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

-   [<span data-ttu-id="2fd70-105">Alterações de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2fd70-105">Header Changes</span></span>](#header-changes)
-   [<span data-ttu-id="2fd70-106">Alterações constantes</span><span class="sxs-lookup"><span data-stu-id="2fd70-106">Constant Changes</span></span>](#constant-changes)
-   [<span data-ttu-id="2fd70-107">Namespaces</span><span class="sxs-lookup"><span data-stu-id="2fd70-107">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="2fd70-108">Cargas parciais</span><span class="sxs-lookup"><span data-stu-id="2fd70-108">Partial Loads</span></span>](#partial-loads)
-   [<span data-ttu-id="2fd70-109">Remoção de tipos específicos do Xbox 360</span><span class="sxs-lookup"><span data-stu-id="2fd70-109">Removal of Xbox 360 Specific Types</span></span>](#removal-of-xbox-360-specific-types)
-   [<span data-ttu-id="2fd70-110">Intrínsecos do ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="2fd70-110">ARM-NEON Intrinsics</span></span>](#arm-neon-intrinsics)
-   [<span data-ttu-id="2fd70-111">Permudo</span><span class="sxs-lookup"><span data-stu-id="2fd70-111">Permute</span></span>](#permute)
-   [<span data-ttu-id="2fd70-112">Formulários de modelo</span><span class="sxs-lookup"><span data-stu-id="2fd70-112">Template Forms</span></span>](#template-forms)
-   [<span data-ttu-id="2fd70-113">Funções eliminadas</span><span class="sxs-lookup"><span data-stu-id="2fd70-113">Eliminated Functions</span></span>](#eliminated-functions)
-   [<span data-ttu-id="2fd70-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fd70-114">Related topics</span></span>](#related-topics)

## <a name="header-changes"></a><span data-ttu-id="2fd70-115">Alterações de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2fd70-115">Header Changes</span></span>

<span data-ttu-id="2fd70-116">A biblioteca DirectXMath usa um novo conjunto de cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="2fd70-116">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="2fd70-117">Substitua o cabeçalho xnamath. h por DirectXMath. h e adicione DirectXPackedVector. h para os tipos "GPU embalado".</span><span class="sxs-lookup"><span data-stu-id="2fd70-117">Replace the xnamath.h header with DirectXMath.h and add DirectXPackedVector.h for the “GPU packed” types.</span></span>

<span data-ttu-id="2fd70-118">Os tipos delimitadores do exemplo de colisão do SDK do DirectX em xnacollision. h agora fazem parte da biblioteca DirectXMath em DirectXCollision. h.</span><span class="sxs-lookup"><span data-stu-id="2fd70-118">The bounding types from the DirectX SDK Collision sample in xnacollision.h is now part of the DirectXMath library in DirectXCollision.h.</span></span> <span data-ttu-id="2fd70-119">Eles foram modificados para usar classes C++ em vez de uma API de estilo C.</span><span class="sxs-lookup"><span data-stu-id="2fd70-119">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="2fd70-120">Alterações constantes</span><span class="sxs-lookup"><span data-stu-id="2fd70-120">Constant Changes</span></span>

<span data-ttu-id="2fd70-121">\_A versão XNAMATH (200, 201, 202, 203, 204 e assim por diante) foi substituída pela \_ versão DIRECXTMATH (300, 301, 302, 303 e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="2fd70-121">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!Note]  
> <span data-ttu-id="2fd70-122">DirectXMath 3, 0 e 3, 2 fornecidos com versões preliminares do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2fd70-122">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="2fd70-123">O DirectXMath 3, 3 está na versão final do SDK do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2fd70-123">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

 

## <a name="namespaces"></a><span data-ttu-id="2fd70-124">Namespaces</span><span class="sxs-lookup"><span data-stu-id="2fd70-124">Namespaces</span></span>

<span data-ttu-id="2fd70-125">A biblioteca DirectXMath usa namespaces C++ para organizar os tipos.</span><span class="sxs-lookup"><span data-stu-id="2fd70-125">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="2fd70-126">O XNA Math usou apenas o namespace global.</span><span class="sxs-lookup"><span data-stu-id="2fd70-126">XNA Math used only the global namespace.</span></span> <span data-ttu-id="2fd70-127">Os tipos DirectXMath em comum com o XNA Math estão no namespace "DirectX" ou "DirectX::P ackedVector".</span><span class="sxs-lookup"><span data-stu-id="2fd70-127">The DirectXMath types in common with XNA Math are in the “DirectX” or the “DirectX::PackedVector” namespace.</span></span>

<span data-ttu-id="2fd70-128">Em arquivos de origem C++, uma solução simples é adicionar instruções ' Using ':</span><span class="sxs-lookup"><span data-stu-id="2fd70-128">In C++ source files, a simple solution is to add ‘using’ statements:</span></span>


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



<span data-ttu-id="2fd70-129">Para cabeçalhos, não é considerada "melhor prática" para adicionar usando instruções.</span><span class="sxs-lookup"><span data-stu-id="2fd70-129">For headers, it is not considered ‘best practice’ to add using statements.</span></span> <span data-ttu-id="2fd70-130">Em vez disso, adicione namespaces totalmente qualificados:</span><span class="sxs-lookup"><span data-stu-id="2fd70-130">Instead, add fully qualified namespaces:</span></span>


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a><span data-ttu-id="2fd70-131">Cargas parciais</span><span class="sxs-lookup"><span data-stu-id="2fd70-131">Partial Loads</span></span>

<span data-ttu-id="2fd70-132">Para várias funções que carregam menos de 4 elementos de um XMVECTOR, a biblioteca de matemática do XNA deixou os elementos adicionais indefinidos.</span><span class="sxs-lookup"><span data-stu-id="2fd70-132">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="2fd70-133">DirectXMath sempre preencherá esses elementos adicionais com 0.</span><span class="sxs-lookup"><span data-stu-id="2fd70-133">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="2fd70-134">Remoção de tipos específicos do Xbox 360</span><span class="sxs-lookup"><span data-stu-id="2fd70-134">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="2fd70-135">Os seguintes tipos de biblioteca matemática do XNA, funções e constantes não estão disponíveis no DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="2fd70-135">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="2fd70-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="2fd70-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="2fd70-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="2fd70-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="2fd70-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="2fd70-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="2fd70-139">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="2fd70-139">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="2fd70-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="2fd70-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="2fd70-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="2fd70-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="2fd70-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="2fd70-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="2fd70-143">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="2fd70-143">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="2fd70-144">\_\_vector4i foi preterido.</span><span class="sxs-lookup"><span data-stu-id="2fd70-144">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="2fd70-145">Em vez disso, use [**XMVECTORI32**](xmvectori32-data-type.md) ou [**XMVECTORU32**](xmvectoru32-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd70-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="2fd70-146">As funções e os tipos a seguir são preteridos, pois são apenas o Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="2fd70-146">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="2fd70-147">Intrínsecos do ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="2fd70-147">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="2fd70-148">A declaração de uma constante de vetor com esse código será compilada para o XNA Math para SSE e não INTRÍNSECOs, mas falhará para DirectXMath usando ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="2fd70-148">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



<span data-ttu-id="2fd70-149">Em geral, não recomendamos esse método de inicialização de um [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2fd70-149">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="2fd70-150">No entanto, se você quiser uma constante de vetor, a classe [**XMVECTORF32**](xmvectorf32-data-type.md) dará suporte a esse estilo de inicialização e retornará o tipo **XMVECTOR** automaticamente para que você possa usar o **XMVECTORF32** na maioria dos mesmos contextos.</span><span class="sxs-lookup"><span data-stu-id="2fd70-150">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="2fd70-151">Qualquer operação de gravação em uma classe **XMVECTORF32** requer a referência explícita ao membro. v **XMVECTOR** .</span><span class="sxs-lookup"><span data-stu-id="2fd70-151">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="2fd70-152">Permudo</span><span class="sxs-lookup"><span data-stu-id="2fd70-152">Permute</span></span>

<span data-ttu-id="2fd70-153">A biblioteca de matemática do XNA tinha o seguinte formato para o vetor geral permudo:</span><span class="sxs-lookup"><span data-stu-id="2fd70-153">The XNA Math library had the following form for general vector permute:</span></span>


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



<span data-ttu-id="2fd70-154">Para DirectXMath, **XMVectorPermuteControl** foi eliminado e o XM \_ permudo \_ 0x..</span><span class="sxs-lookup"><span data-stu-id="2fd70-154">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="2fd70-155">As \_ constantes do XM permudo \_ 1Z foram redefinidas para índices simples 0-7.</span><span class="sxs-lookup"><span data-stu-id="2fd70-155">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="2fd70-156">Aqui está a nova assinatura para [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span><span class="sxs-lookup"><span data-stu-id="2fd70-156">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



<span data-ttu-id="2fd70-157">Em vez de uma palavra de controle, essa função usa diretamente os quatro índices como parâmetros, o que também o torna análogo à função [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) usando o novo XM \_ SWIZZLE \_ X.</span><span class="sxs-lookup"><span data-stu-id="2fd70-157">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="2fd70-158">XM \_ SWIZZLE \_ W as constantes definidas como índices simples 0-3.</span><span class="sxs-lookup"><span data-stu-id="2fd70-158">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> <span data-ttu-id="2fd70-159">Para valores constantes, há uma maneira muito mais eficiente de implementar o permudo.</span><span class="sxs-lookup"><span data-stu-id="2fd70-159">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="2fd70-160">Em vez de usar a forma de função de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use o formulário de **modelo** :</span><span class="sxs-lookup"><span data-stu-id="2fd70-160">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a><span data-ttu-id="2fd70-161">Formulários de modelo</span><span class="sxs-lookup"><span data-stu-id="2fd70-161">Template Forms</span></span>
>
> <span data-ttu-id="2fd70-162">Em geral, o uso de um formulário de modelo sobre uma forma de função das funções a seguir é muito mais eficiente e permite que a biblioteca faça otimizações específicas da plataforma por meio de especialização de modelo.</span><span class="sxs-lookup"><span data-stu-id="2fd70-162">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a><span data-ttu-id="2fd70-163">Funções eliminadas</span><span class="sxs-lookup"><span data-stu-id="2fd70-163">Eliminated Functions</span></span>
>
> 
>
> | <span data-ttu-id="2fd70-164">Função eliminada</span><span class="sxs-lookup"><span data-stu-id="2fd70-164">Eliminated Function</span></span>        | <span data-ttu-id="2fd70-165">Substituição</span><span class="sxs-lookup"><span data-stu-id="2fd70-165">Replacement</span></span>                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | <span data-ttu-id="2fd70-166">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="2fd70-166">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="2fd70-167">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="2fd70-167">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | <span data-ttu-id="2fd70-168">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="2fd70-168">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="2fd70-169">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="2fd70-169">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | <span data-ttu-id="2fd70-170">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="2fd70-170">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="2fd70-171">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="2fd70-171">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | <span data-ttu-id="2fd70-172">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="2fd70-172">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="2fd70-173">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="2fd70-173">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | <span data-ttu-id="2fd70-174">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="2fd70-174">XMStoreInt4NC</span></span>              | [<span data-ttu-id="2fd70-175">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="2fd70-175">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | <span data-ttu-id="2fd70-176">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="2fd70-176">XMVector2InBoundsR</span></span>         | <span data-ttu-id="2fd70-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="2fd70-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="2fd70-178">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="2fd70-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="2fd70-179">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="2fd70-179">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="2fd70-180">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="2fd70-180">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | <span data-ttu-id="2fd70-181">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="2fd70-181">XMVector3InBoundsR</span></span>         | <span data-ttu-id="2fd70-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="2fd70-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="2fd70-183">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="2fd70-183">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="2fd70-184">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="2fd70-184">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="2fd70-185">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="2fd70-185">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | <span data-ttu-id="2fd70-186">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="2fd70-186">XMVector4InBoundsR</span></span>         | <span data-ttu-id="2fd70-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="2fd70-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="2fd70-188">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="2fd70-188">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="2fd70-189">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="2fd70-189">XMVectorCosHEst</span></span>            | [<span data-ttu-id="2fd70-190">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="2fd70-190">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | <span data-ttu-id="2fd70-191">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="2fd70-191">XMVectorExpEst</span></span>             | [<span data-ttu-id="2fd70-192">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="2fd70-192">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | <span data-ttu-id="2fd70-193">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="2fd70-193">XMVectorLogEst</span></span>             | [<span data-ttu-id="2fd70-194">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="2fd70-194">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | <span data-ttu-id="2fd70-195">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="2fd70-195">XMVectorPowEst</span></span>             | [<span data-ttu-id="2fd70-196">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="2fd70-196">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | <span data-ttu-id="2fd70-197">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="2fd70-197">XMVectorSinHEst</span></span>            | [<span data-ttu-id="2fd70-198">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="2fd70-198">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | <span data-ttu-id="2fd70-199">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="2fd70-199">XMVectorTanHEst</span></span>            | [<span data-ttu-id="2fd70-200">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="2fd70-200">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a><span data-ttu-id="2fd70-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fd70-201">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="2fd70-202">Guia de programação do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="2fd70-202">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
