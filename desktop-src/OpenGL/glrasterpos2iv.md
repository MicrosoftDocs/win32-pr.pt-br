---
title: função glRasterPos2iv (GL. h)
description: Especifica a posição da varredura para operações de pixel. | função glRasterPos2iv (GL. h)
ms.assetid: 0e54681f-f2da-4b29-a3ea-a51775a68c98
keywords:
- função glRasterPos2dv OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c6fc9de21762adb8f932677c61920578a28ad4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930421"
---
# <a name="glrasterpos2iv-function"></a><span data-ttu-id="d7b9b-105">função glRasterPos2iv</span><span class="sxs-lookup"><span data-stu-id="d7b9b-105">glRasterPos2iv function</span></span>

<span data-ttu-id="d7b9b-106">Especifica a posição da varredura para operações de pixel.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b9b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7b9b-107">Syntax</span></span>


```C++
void WINAPI glRasterPos2dv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="d7b9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7b9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b9b-109">*l*</span><span class="sxs-lookup"><span data-stu-id="d7b9b-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b9b-110">Um ponteiro para uma matriz de dois elementos, especificando coordenadas x e y para a posição de rasterização atual.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-110">A pointer to an array of two elements, specifying x and y coordinates for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b9b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7b9b-111">Return value</span></span>

<span data-ttu-id="d7b9b-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7b9b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7b9b-113">Remarks</span></span>

<span data-ttu-id="d7b9b-114">O OpenGL mantém uma posição de 3D em coordenadas de janela.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-114">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="d7b9b-115">Essa posição, chamada de posição de rasterização, é mantida com precisão de subpixel.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-115">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="d7b9b-116">Ele é usado para posicionar operações de gravação de pixel e bitmap.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-116">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="d7b9b-117">Consulte [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)e [**glCopyPixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="d7b9b-117">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="d7b9b-118">A posição de rasterização atual consiste em três coordenadas de janela (*x, y, z*), uma coordenada de clipe *w* , uma distância de coordenadas de olho, um bit válido e coordenadas de textura e de dados de cor associadas.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-118">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="d7b9b-119">A coordenada *w* é uma coordenada de clipe, porque *w* não é projetado para coordenadas de janelas.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-119">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="d7b9b-120">A função [glRasterPos4](glrasterpos-functions.md) especifica as coordenadas de objeto *x, y, z* e *w* explicitamente.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-120">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="d7b9b-121">A função glRasterPos3 especifica as coordenadas de objeto *x, y* e *z* explicitamente, enquanto *w* é definido implicitamente como um.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-121">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="d7b9b-122">A função glRasterPos2 usa os valores de argumento para *x* e *y* enquanto configura implicitamente *z* e *w* como zero e um.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-122">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="d7b9b-123">As coordenadas de objeto apresentadas por [glRasterPos](glrasterpos-functions.md) são tratadas exatamente como as de um comando [glVertex](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="d7b9b-123">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="d7b9b-124">Elas são transformadas pelas matrizes de modelview e projeção atuais e passadas para o estágio de recorte.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-124">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="d7b9b-125">Se o vértice não for remarcado, ele será projetado e dimensionado para as coordenadas da janela, que se tornarão a nova posição de varredura atual e \_ o \_ sinalizador válido da posição de varredura atual do GL \_ \_ estiver definido.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-125">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="d7b9b-126">Se o vértice for removido, o bit válido será limpo e a posição atual da varredura e as coordenadas de cor e textura associadas serão indefinidas.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-126">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="d7b9b-127">A posição de rasterização atual também inclui alguns dados de cor e coordenadas de textura associados.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-127">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="d7b9b-128">Se a iluminação estiver habilitada, \_ \_ a cor de rasterização atual do GL \_ , no modo RGBA ou no \_ índice de varredura atual GL \_ \_ , no modo de índice de cor, será definida como a cor produzida pelo cálculo de iluminação (consulte [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)e [**glShadeModel**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="d7b9b-128">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="d7b9b-129">Se a iluminação estiver desabilitada, a cor atual (no modo RGBA, a cor atual do estado do GL \_ \_ ) ou o índice de cores (no modo de índice de cor, índice atual GL de variável de estado \_ \_ ) será usado para atualizar a cor de varredura atual.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-129">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="d7b9b-130">Da mesma forma, GL \_ \_ CoOrds de textura de rasterização atual \_ \_ é atualizado como uma função de \_ CoOrds de textura atual do GL \_ \_ , com base na matriz de textura e nas funções de geração de textura (consulte [glTexGen](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="d7b9b-130">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="d7b9b-131">Por fim, a distância da origem do sistema de coordenadas de olho ao vértice, como transformado apenas pela matriz modelview, substitui a \_ distância de varredura atual do GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d7b9b-131">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="d7b9b-132">Inicialmente, a posição de rasterização atual é (0, 0, 0, 1), a distância de varredura atual é 0, o bit válido é definido, a cor RGBA associada é (1, 1, 1, 1), o índice de cor associado é 1 e as coordenadas de textura associadas são (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="d7b9b-132">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="d7b9b-133">No modo RGBA, \_ \_ o índice de varredura atual \_ do GL é sempre 1; no modo de índice de cor, a cor RGBA atual sempre mantém seu valor inicial.</span><span class="sxs-lookup"><span data-stu-id="d7b9b-133">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="d7b9b-134">A posição da rasterização é modificada por [glRasterPos](glrasterpos-functions.md) e por [**glBitmap**](glbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="d7b9b-134">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="d7b9b-135">Quando as coordenadas de posição de rasterização são inválidas, os comandos de desenho baseados na posição de rasterização são ignorados (ou seja, eles não resultam em alterações no estado OpenGL).</span><span class="sxs-lookup"><span data-stu-id="d7b9b-135">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="d7b9b-136">As funções a seguir recuperam informações relacionadas ao [glRasterPos](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="d7b9b-136">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="d7b9b-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de rasterização atual \_</span><span class="sxs-lookup"><span data-stu-id="d7b9b-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="d7b9b-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ posição de rasterização atual \_ \_ válida</span><span class="sxs-lookup"><span data-stu-id="d7b9b-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="d7b9b-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL a \_ \_ distância de rasterização atual \_</span><span class="sxs-lookup"><span data-stu-id="d7b9b-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="d7b9b-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ cor de rasterização atual \_</span><span class="sxs-lookup"><span data-stu-id="d7b9b-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="d7b9b-141">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ índice de varredura atual glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="d7b9b-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="d7b9b-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ textura de rasterização atual \_ \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="d7b9b-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="d7b9b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7b9b-143">Requirements</span></span>



| <span data-ttu-id="d7b9b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7b9b-144">Requirement</span></span> | <span data-ttu-id="d7b9b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="d7b9b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b9b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b9b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b9b-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7b9b-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d7b9b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b9b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b9b-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7b9b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7b9b-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d7b9b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7b9b-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7b9b-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d7b9b-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7b9b-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7b9b-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7b9b-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7b9b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="d7b9b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7b9b-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7b9b-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b9b-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7b9b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b9b-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d7b9b-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-158">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="d7b9b-158">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="d7b9b-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="d7b9b-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d7b9b-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-162">glLight</span><span class="sxs-lookup"><span data-stu-id="d7b9b-162">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-163">glLightModel</span><span class="sxs-lookup"><span data-stu-id="d7b9b-163">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-164">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="d7b9b-164">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-165">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="d7b9b-165">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-166">glTexGen</span><span class="sxs-lookup"><span data-stu-id="d7b9b-166">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="d7b9b-167">glVertex</span><span class="sxs-lookup"><span data-stu-id="d7b9b-167">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





