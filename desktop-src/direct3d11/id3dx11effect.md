---
title: Interface ID3DX11Effect (D3dx11effect. h)
description: Uma interface ID3DX11Effect gerencia um conjunto de objetos de estado, recursos e sombreadores para implementar um efeito de renderização.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Interface ID3DX11Effect Direct3D 11
- Interface ID3DX11Effect Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51c9b945f09ad0424ecd6b546aefe68bea276ffc
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314449"
---
# <a name="id3dx11effect-interface"></a><span data-ttu-id="dfddc-105">Interface ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="dfddc-105">ID3DX11Effect interface</span></span>

<span data-ttu-id="dfddc-106">Uma interface **ID3DX11Effect** gerencia um conjunto de objetos de estado, recursos e sombreadores para implementar um efeito de renderização.</span><span class="sxs-lookup"><span data-stu-id="dfddc-106">An **ID3DX11Effect** interface manages a set of state objects, resources, and shaders for implementing a rendering effect.</span></span>

## <a name="members"></a><span data-ttu-id="dfddc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="dfddc-107">Members</span></span>

<span data-ttu-id="dfddc-108">A interface **ID3DX11Effect** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dfddc-108">The **ID3DX11Effect** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dfddc-109">**ID3DX11Effect** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dfddc-109">**ID3DX11Effect** also has these types of members:</span></span>

-   [<span data-ttu-id="dfddc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfddc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dfddc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfddc-111">Methods</span></span>

<span data-ttu-id="dfddc-112">A interface **ID3DX11Effect** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dfddc-112">The **ID3DX11Effect** interface has these methods.</span></span>



| <span data-ttu-id="dfddc-113">Método</span><span class="sxs-lookup"><span data-stu-id="dfddc-113">Method</span></span>                                                                     | <span data-ttu-id="dfddc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfddc-114">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfddc-115">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="dfddc-115">**CloneEffect**</span></span>](id3dx11effect-cloneeffect.md)                           | <span data-ttu-id="dfddc-116">Cria uma cópia de uma interface de efeito.</span><span class="sxs-lookup"><span data-stu-id="dfddc-116">Creates a copy of an effect interface.</span></span><br/>                                         |
| [<span data-ttu-id="dfddc-117">**GetClassLinkage**</span><span class="sxs-lookup"><span data-stu-id="dfddc-117">**GetClassLinkage**</span></span>](id3dx11effect-getclasslinkage.md)                   | <span data-ttu-id="dfddc-118">Obtém uma interface de vinculação de classe.</span><span class="sxs-lookup"><span data-stu-id="dfddc-118">Gets a class linkage interface.</span></span><br/>                                                |
| [<span data-ttu-id="dfddc-119">**GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="dfddc-119">**GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md) | <span data-ttu-id="dfddc-120">Obtenha um buffer constante por índice.</span><span class="sxs-lookup"><span data-stu-id="dfddc-120">Get a constant buffer by index.</span></span><br/>                                                |
| [<span data-ttu-id="dfddc-121">**GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="dfddc-121">**GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)   | <span data-ttu-id="dfddc-122">Obtenha um buffer constante por nome.</span><span class="sxs-lookup"><span data-stu-id="dfddc-122">Get a constant buffer by name.</span></span><br/>                                                 |
| [<span data-ttu-id="dfddc-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="dfddc-123">**GetDesc**</span></span>](id3dx11effect-getdesc.md)                                   | <span data-ttu-id="dfddc-124">Obtenha uma descrição de efeito.</span><span class="sxs-lookup"><span data-stu-id="dfddc-124">Get an effect description.</span></span><br/>                                                     |
| [<span data-ttu-id="dfddc-125">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="dfddc-125">**GetDevice**</span></span>](id3dx11effect-getdevice.md)                               | <span data-ttu-id="dfddc-126">Obtenha o dispositivo que criou o efeito.</span><span class="sxs-lookup"><span data-stu-id="dfddc-126">Get the device that created the effect.</span></span><br/>                                        |
| [<span data-ttu-id="dfddc-127">**GetGroupByIndex**</span><span class="sxs-lookup"><span data-stu-id="dfddc-127">**GetGroupByIndex**</span></span>](id3dx11effect-getgroupbyindex.md)                   | <span data-ttu-id="dfddc-128">Obtém um grupo de efeitos por índice.</span><span class="sxs-lookup"><span data-stu-id="dfddc-128">Gets an effect group by index.</span></span><br/>                                                 |
| [<span data-ttu-id="dfddc-129">**Getgroupbyname**</span><span class="sxs-lookup"><span data-stu-id="dfddc-129">**GetGroupByName**</span></span>](id3dx11effect-getgroupbyname.md)                     | <span data-ttu-id="dfddc-130">Obtém um grupo de efeitos por nome.</span><span class="sxs-lookup"><span data-stu-id="dfddc-130">Gets an effect group by name.</span></span><br/>                                                  |
| [<span data-ttu-id="dfddc-131">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="dfddc-131">**GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)           | <span data-ttu-id="dfddc-132">Obtenha uma técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="dfddc-132">Get a technique by index.</span></span><br/>                                                      |
| [<span data-ttu-id="dfddc-133">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="dfddc-133">**GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)             | <span data-ttu-id="dfddc-134">Obtenha uma técnica por nome.</span><span class="sxs-lookup"><span data-stu-id="dfddc-134">Get a technique by name.</span></span><br/>                                                       |
| [<span data-ttu-id="dfddc-135">**GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="dfddc-135">**GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)             | <span data-ttu-id="dfddc-136">Obter uma variável por índice.</span><span class="sxs-lookup"><span data-stu-id="dfddc-136">Get a variable by index.</span></span><br/>                                                       |
| [<span data-ttu-id="dfddc-137">**GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="dfddc-137">**GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)               | <span data-ttu-id="dfddc-138">Obter uma variável por nome.</span><span class="sxs-lookup"><span data-stu-id="dfddc-138">Get a variable by name.</span></span><br/>                                                        |
| [<span data-ttu-id="dfddc-139">**GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="dfddc-139">**GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)       | <span data-ttu-id="dfddc-140">Obter uma variável por semântica.</span><span class="sxs-lookup"><span data-stu-id="dfddc-140">Get a variable by semantic.</span></span><br/>                                                    |
| [<span data-ttu-id="dfddc-141">**Isoptimized**</span><span class="sxs-lookup"><span data-stu-id="dfddc-141">**IsOptimized**</span></span>](id3dx11effect-isoptimized.md)                           | <span data-ttu-id="dfddc-142">Teste um efeito para ver se os metadados de reflexão foram removidos da memória.</span><span class="sxs-lookup"><span data-stu-id="dfddc-142">Test an effect to see if the reflection metadata has been removed from memory.</span></span><br/> |
| [<span data-ttu-id="dfddc-143">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="dfddc-143">**IsValid**</span></span>](id3dx11effect-isvalid.md)                                   | <span data-ttu-id="dfddc-144">Teste um efeito para ver se ele contém uma sintaxe válida.</span><span class="sxs-lookup"><span data-stu-id="dfddc-144">Test an effect to see if it contains valid syntax.</span></span><br/>                             |
| [<span data-ttu-id="dfddc-145">**Otimizar**</span><span class="sxs-lookup"><span data-stu-id="dfddc-145">**Optimize**</span></span>](id3dx11effect-optimize.md)                                 | <span data-ttu-id="dfddc-146">Minimize a quantidade de memória necessária para um efeito.</span><span class="sxs-lookup"><span data-stu-id="dfddc-146">Minimize the amount of memory required for an effect.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="dfddc-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfddc-147">Remarks</span></span>

<span data-ttu-id="dfddc-148">Um efeito é criado chamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="dfddc-148">An effect is created by calling [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

<span data-ttu-id="dfddc-149">O sistema de efeitos agrupa as informações necessárias para a renderização em um efeito que contém: objetos de estado para a atribuição de alterações de estado em grupos, recursos para fornecer dados de entrada e armazenamento de dados de saída, e programas que controlam como a renderização é feita chamada de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="dfddc-149">The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders.</span></span>

> [!Note]  
> <span data-ttu-id="dfddc-150">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="dfddc-150">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="dfddc-151">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="dfddc-151">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="dfddc-152">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="dfddc-152">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

> [!Note]
>
> <span data-ttu-id="dfddc-153">Se você chamar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um objeto **ID3DX11Effect** para recuperar a interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , **QueryInterface** retornará E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="dfddc-153">If you call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an **ID3DX11Effect** object to retrieve the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, **QueryInterface** returns E\_NOINTERFACE.</span></span> <span data-ttu-id="dfddc-154">Para contornar esse problema, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="dfddc-154">To work around this issue, use the following code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>>
>  

## <a name="requirements"></a><span data-ttu-id="dfddc-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfddc-155">Requirements</span></span>

| <span data-ttu-id="dfddc-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfddc-156">Requirement</span></span> | <span data-ttu-id="dfddc-157">Valor</span><span class="sxs-lookup"><span data-stu-id="dfddc-157">Value</span></span> |
|-------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfddc-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfddc-158">Header</span></span><br/>  | <dl> <span data-ttu-id="dfddc-159"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfddc-159"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="dfddc-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dfddc-160">Library</span></span><br/> | <dl> <span data-ttu-id="dfddc-161"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="dfddc-161"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="dfddc-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfddc-162">See also</span></span>

[<span data-ttu-id="dfddc-163">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="dfddc-163">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)

[<span data-ttu-id="dfddc-164">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="dfddc-164">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
