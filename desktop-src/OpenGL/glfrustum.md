---
title: função glFrustum (GL. h)
description: A função glFrustum multiplica a matriz atual por uma matriz de perspectiva.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- função glFrustum OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104553450"
---
# <a name="glfrustum-function"></a><span data-ttu-id="4b90a-104">função glFrustum</span><span class="sxs-lookup"><span data-stu-id="4b90a-104">glFrustum function</span></span>

<span data-ttu-id="4b90a-105">A função **glFrustum** multiplica a matriz atual por uma matriz de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="4b90a-105">The **glFrustum** function multiplies the current matrix by a perspective matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b90a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b90a-106">Syntax</span></span>


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="4b90a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b90a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b90a-108">*esquerda*</span><span class="sxs-lookup"><span data-stu-id="4b90a-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="4b90a-109">A coordenada para o plano de recorte vertical esquerdo.</span><span class="sxs-lookup"><span data-stu-id="4b90a-109">The coordinate for the left-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="4b90a-110">*direita*</span><span class="sxs-lookup"><span data-stu-id="4b90a-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="4b90a-111">A coordenada do plano de recorte vertical à direita.</span><span class="sxs-lookup"><span data-stu-id="4b90a-111">The coordinate for the right-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="4b90a-112">*parte inferior*</span><span class="sxs-lookup"><span data-stu-id="4b90a-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="4b90a-113">A coordenada do plano de recorte inferior horizontal.</span><span class="sxs-lookup"><span data-stu-id="4b90a-113">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="4b90a-114">*início*</span><span class="sxs-lookup"><span data-stu-id="4b90a-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="4b90a-115">A coordenada do plano de recorte inferior horizontal.</span><span class="sxs-lookup"><span data-stu-id="4b90a-115">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="4b90a-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="4b90a-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="4b90a-117">As distâncias para o plano de recorte quase aprofundado.</span><span class="sxs-lookup"><span data-stu-id="4b90a-117">The distances to the near-depth clipping plane.</span></span> <span data-ttu-id="4b90a-118">Deve ser positivo.</span><span class="sxs-lookup"><span data-stu-id="4b90a-118">Must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="4b90a-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="4b90a-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="4b90a-120">As distâncias para os planos de recorte muito detalhados.</span><span class="sxs-lookup"><span data-stu-id="4b90a-120">The distances to the far-depth clipping planes.</span></span> <span data-ttu-id="4b90a-121">Deve ser positivo.</span><span class="sxs-lookup"><span data-stu-id="4b90a-121">Must be positive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b90a-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b90a-122">Return value</span></span>

<span data-ttu-id="4b90a-123">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4b90a-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b90a-124">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4b90a-124">Error codes</span></span>

<span data-ttu-id="4b90a-125">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4b90a-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4b90a-126">Nome</span><span class="sxs-lookup"><span data-stu-id="4b90a-126">Name</span></span>                                                                                                  | <span data-ttu-id="4b90a-127">Significado</span><span class="sxs-lookup"><span data-stu-id="4b90a-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b90a-128"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="4b90a-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4b90a-129">*zNear* ou *zFar* não era postitive.</span><span class="sxs-lookup"><span data-stu-id="4b90a-129">*zNear* or *zFar* was not postitive.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="4b90a-130"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4b90a-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4b90a-131">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4b90a-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4b90a-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b90a-132">Remarks</span></span>

<span data-ttu-id="4b90a-133">A função **glFrustum** descreve uma matriz de perspectiva que produz uma projeção de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="4b90a-133">The **glFrustum** function describes a perspective matrix that produces a perspective projection.</span></span> <span data-ttu-id="4b90a-134">Os parâmetros (*esquerda*, *inferior*, *zNear*) e (*direita*, *superior*, *zNear*) especificam os pontos no plano de recorte próximo que são mapeados para os cantos inferior esquerdo e superior direito da janela, respectivamente, supondo que o olho está localizado em (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="4b90a-134">The (*left*, *bottom*, *zNear*) and (*right*, *top*, *zNear*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0,0,0).</span></span> <span data-ttu-id="4b90a-135">O parâmetro *zFar* especifica o local do plano de recorte distante.</span><span class="sxs-lookup"><span data-stu-id="4b90a-135">The *zFar* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="4b90a-136">*ZNear* e *zFar* devem ser positivos.</span><span class="sxs-lookup"><span data-stu-id="4b90a-136">Both *zNear* and *zFar* must be positive.</span></span> <span data-ttu-id="4b90a-137">A matriz correspondente é mostrada na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b90a-137">The corresponding matrix is shown in the following image.</span></span>

![Diagrama que mostra a matriz de perspectiva que produz uma projeção em perspectiva.](images/frust01.png)![Equações mostrando a função glFrustum que descreve uma matriz de perspectiva.](images/frust02.png)

<span data-ttu-id="4b90a-140">A função **glFrustum** multiplica a matriz atual por esta matriz, com o resultado que substitui a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="4b90a-140">The **glFrustum** function multiplies the current matrix by this matrix, with the result replacing the current matrix.</span></span> <span data-ttu-id="4b90a-141">Ou seja, se M for a matriz atual e F for a matriz de perspectiva frustum, **glFrustum** substituirá M por m F.</span><span class="sxs-lookup"><span data-stu-id="4b90a-141">That is, if M is the current matrix and F is the frustum perspective matrix, then **glFrustum** replaces M with M   F.</span></span>

<span data-ttu-id="4b90a-142">Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar a pilha de matriz atual.</span><span class="sxs-lookup"><span data-stu-id="4b90a-142">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the current matrix stack.</span></span>

<span data-ttu-id="4b90a-143">A precisão do buffer de profundidade é afetada pelos valores especificados para *zNear* e *zFar*.</span><span class="sxs-lookup"><span data-stu-id="4b90a-143">Depth-buffer precision is affected by the values specified for *zNear* and *zFar*.</span></span> <span data-ttu-id="4b90a-144">Quanto maior a proporção de *zFar* para *zNear* , menor será o buffer de profundidade em relação à distinção entre as superfícies que estão próximas umas das outras.</span><span class="sxs-lookup"><span data-stu-id="4b90a-144">The greater the ratio of *zFar* to *zNear* is, the less effective the depth buffer will be at distinguishing between surfaces that are near each other.</span></span> <span data-ttu-id="4b90a-145">If</span><span class="sxs-lookup"><span data-stu-id="4b90a-145">If</span></span>

![Equação mostrando a proporção de até o próximo.](images/frust03.png)

<span data-ttu-id="4b90a-147">aproximadamente *log* 2 (*r*) partes de precisão do buffer de profundidade são perdidas.</span><span class="sxs-lookup"><span data-stu-id="4b90a-147">roughly *log* 2 (*r*) bits of depth buffer precision are lost.</span></span> <span data-ttu-id="4b90a-148">Como o *r* se aproxima do infinito, uma vez que o *zNear* se aproxima de zero, você nunca deve definir *zNear* como zero.</span><span class="sxs-lookup"><span data-stu-id="4b90a-148">Because *r* approaches infinity as *zNear* approaches zero, you should never set *zNear* to zero.</span></span>

<span data-ttu-id="4b90a-149">As seguintes funções recuperam informações sobre **glFrustum**:</span><span class="sxs-lookup"><span data-stu-id="4b90a-149">The following functions retrieve information about **glFrustum**:</span></span>

<span data-ttu-id="4b90a-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="4b90a-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="4b90a-151">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="4b90a-151">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="4b90a-152"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="4b90a-152">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="4b90a-153">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="4b90a-153">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="4b90a-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b90a-154">Requirements</span></span>



| <span data-ttu-id="4b90a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b90a-155">Requirement</span></span> | <span data-ttu-id="4b90a-156">Valor</span><span class="sxs-lookup"><span data-stu-id="4b90a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b90a-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b90a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4b90a-158">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4b90a-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4b90a-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b90a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4b90a-160">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4b90a-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b90a-161">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4b90a-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b90a-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b90a-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4b90a-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b90a-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b90a-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b90a-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4b90a-165">DLL</span><span class="sxs-lookup"><span data-stu-id="4b90a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b90a-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b90a-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b90a-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b90a-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b90a-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4b90a-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4b90a-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4b90a-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4b90a-170">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4b90a-170">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4b90a-171">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="4b90a-171">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="4b90a-172">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="4b90a-172">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="4b90a-173">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="4b90a-173">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="4b90a-174">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="4b90a-174">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="4b90a-175">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="4b90a-175">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="4b90a-176">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="4b90a-176">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





