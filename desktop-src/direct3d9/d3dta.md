---
description: 'As constantes de argumento de textura são usadas como valores para os seguintes membros do tipo enumerado D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58d4d5665b1a098b84eaa95294e69220d6ea4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793945"
---
# <a name="d3dta"></a><span data-ttu-id="c7b47-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="c7b47-103">D3DTA</span></span>

<span data-ttu-id="c7b47-104">As constantes de argumento de textura são usadas como valores para os seguintes membros do tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) :</span><span class="sxs-lookup"><span data-stu-id="c7b47-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="c7b47-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="c7b47-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="c7b47-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="c7b47-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="c7b47-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="c7b47-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="c7b47-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="c7b47-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="c7b47-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="c7b47-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="c7b47-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="c7b47-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="c7b47-111">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="c7b47-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="c7b47-112">Defina e recupere argumentos de textura chamando os métodos [**SetTextureStageState**](/windows/desktop/api) e [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="c7b47-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="c7b47-113">Sinalizadores de argumento</span><span class="sxs-lookup"><span data-stu-id="c7b47-113">Argument flags</span></span>

<span data-ttu-id="c7b47-114">Você pode combinar um sinalizador de argumento com um modificador, mas não é possível combinar dois sinalizadores de argumento.</span><span class="sxs-lookup"><span data-stu-id="c7b47-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b47-115">\#definir</span><span class="sxs-lookup"><span data-stu-id="c7b47-115">\#define</span></span>          | <span data-ttu-id="c7b47-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7b47-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c7b47-117">\_Constante D3DTA</span><span class="sxs-lookup"><span data-stu-id="c7b47-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="c7b47-118">Selecione uma constante em um estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="c7b47-119">O valor padrão é 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c7b47-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c7b47-120">D3DTA \_ atual</span><span class="sxs-lookup"><span data-stu-id="c7b47-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="c7b47-121">O argumento de textura é o resultado do estágio de mesclagem anterior.</span><span class="sxs-lookup"><span data-stu-id="c7b47-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="c7b47-122">No primeiro estágio de textura (estágio 0), esse argumento é equivalente a D3DTA \_ difuso.</span><span class="sxs-lookup"><span data-stu-id="c7b47-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="c7b47-123">Se o estágio de mesclagem anterior usar uma textura de mapa de relevo (a \_ operação D3DTOP BUMPENVMAP), o sistema escolherá a textura do palco antes da textura do mapa de choques.</span><span class="sxs-lookup"><span data-stu-id="c7b47-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="c7b47-124">Se s representa o estágio de textura atual e o s-1 contiver uma textura de mapa de relevo, esse argumento se tornará a saída de resultado pelo estágio de textura s-2.</span><span class="sxs-lookup"><span data-stu-id="c7b47-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="c7b47-125">As permissões são de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c7b47-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="c7b47-126">D3DTA \_ difuso</span><span class="sxs-lookup"><span data-stu-id="c7b47-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="c7b47-127">O argumento de textura é a cor difusa interpolada dos componentes de vértice durante o sombreamento de Gouraud.</span><span class="sxs-lookup"><span data-stu-id="c7b47-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="c7b47-128">Se o vértice não contiver uma cor difusa, a cor padrão será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c7b47-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="c7b47-129">As permissões são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c7b47-130">D3DTA \_ SELECTMASK</span><span class="sxs-lookup"><span data-stu-id="c7b47-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="c7b47-131">Valor de Mask para todos os argumentos; Não usado ao definir argumentos de textura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c7b47-132">\_Especular D3DTA</span><span class="sxs-lookup"><span data-stu-id="c7b47-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="c7b47-133">O argumento de textura é a cor especular interpolada dos componentes de vértice durante o sombreamento de Gouraud.</span><span class="sxs-lookup"><span data-stu-id="c7b47-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="c7b47-134">Se o vértice não contiver uma cor especular, a cor padrão será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c7b47-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="c7b47-135">As permissões são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c7b47-136">D3DTA \_ Temp</span><span class="sxs-lookup"><span data-stu-id="c7b47-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="c7b47-137">O argumento de textura é uma cor de registro temporária para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="c7b47-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="c7b47-138">\_O D3DTA Temp terá suporte se a funcionalidade do dispositivo [D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md) estiver presente.</span><span class="sxs-lookup"><span data-stu-id="c7b47-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="c7b47-139">O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="c7b47-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="c7b47-140">As permissões são de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c7b47-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="c7b47-141">\_Textura D3DTA</span><span class="sxs-lookup"><span data-stu-id="c7b47-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="c7b47-142">O argumento de textura é a cor de textura para este estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="c7b47-143">As permissões são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c7b47-144">D3DTA \_ TFACTOR</span><span class="sxs-lookup"><span data-stu-id="c7b47-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="c7b47-145">O argumento de textura é o fator de textura definido em uma chamada anterior para [**Setrenderingstate**](/windows/desktop/api) com o valor de [**D3DRS \_ TEXTUREFACTOR**](./d3drenderstatetype.md) render-State.</span><span class="sxs-lookup"><span data-stu-id="c7b47-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="c7b47-146">As permissões são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="c7b47-147">Sinalizadores de modificador</span><span class="sxs-lookup"><span data-stu-id="c7b47-147">Modifier flags</span></span>

<span data-ttu-id="c7b47-148">Um sinalizador de argumento pode ser combinado com um dos seguintes sinalizadores de modificador.</span><span class="sxs-lookup"><span data-stu-id="c7b47-148">An argument flag may be combined with one of the following modifier flags.</span></span>



|                       |                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b47-149">\#definir</span><span class="sxs-lookup"><span data-stu-id="c7b47-149">\#define</span></span>              | <span data-ttu-id="c7b47-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7b47-150">Description</span></span>                                                                                                    |
| <span data-ttu-id="c7b47-151">D3DTA \_ ALPHAREPLICATE</span><span class="sxs-lookup"><span data-stu-id="c7b47-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="c7b47-152">Replique as informações alfa para todos os canais de cores antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="c7b47-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="c7b47-153">Este é um modificador de leitura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-153">This is a read modifier.</span></span> |
| <span data-ttu-id="c7b47-154">\_Complemento do D3DTA</span><span class="sxs-lookup"><span data-stu-id="c7b47-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="c7b47-155">Adote o complemento do argumento x, (1,0-x).</span><span class="sxs-lookup"><span data-stu-id="c7b47-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="c7b47-156">Este é um modificador de leitura.</span><span class="sxs-lookup"><span data-stu-id="c7b47-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="c7b47-157">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="c7b47-157">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="c7b47-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7b47-158">Header</span></span>                   | <span data-ttu-id="c7b47-159">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="c7b47-159">d3d9types.h</span></span> |
| <span data-ttu-id="c7b47-160">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="c7b47-160">Minimum operating system</span></span> | <span data-ttu-id="c7b47-161">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c7b47-161">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="c7b47-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7b47-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7b47-163">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c7b47-163">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
