---
title: função glOrtho (GL. h)
description: A função glOrtho multiplica a matriz atual por uma matriz ortográfica.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- função glOrtho OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104563235"
---
# <a name="glortho-function"></a><span data-ttu-id="fc9fd-104">função glOrtho</span><span class="sxs-lookup"><span data-stu-id="fc9fd-104">glOrtho function</span></span>

<span data-ttu-id="fc9fd-105">A função **glOrtho** multiplica a matriz atual por uma matriz ortográfica.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-105">The **glOrtho** function multiplies the current matrix by an orthographic matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc9fd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc9fd-106">Syntax</span></span>


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="fc9fd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc9fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc9fd-108">*esquerda*</span><span class="sxs-lookup"><span data-stu-id="fc9fd-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="fc9fd-109">As coordenadas do plano de recorte vertical esquerdo.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-109">The coordinates for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="fc9fd-110">*direita*</span><span class="sxs-lookup"><span data-stu-id="fc9fd-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="fc9fd-111">As coordenadas para o plano de recorte vertical direito.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-111">The coordinates for theright vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="fc9fd-112">*parte inferior*</span><span class="sxs-lookup"><span data-stu-id="fc9fd-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="fc9fd-113">As coordenadas do plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-113">The coordinates for the bottom horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="fc9fd-114">*início*</span><span class="sxs-lookup"><span data-stu-id="fc9fd-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="fc9fd-115">As coordenadas dos principais planos de recorte horizontal.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-115">The coordinates for the top horizontal clipping plans.</span></span>

</dd> <dt>

<span data-ttu-id="fc9fd-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="fc9fd-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="fc9fd-117">As distâncias para o plano de recorte de profundidade mais próxima.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-117">The distances to the nearer depth clipping plane.</span></span> <span data-ttu-id="fc9fd-118">Essa distância será negativa se o plano estiver por trás do visualizador.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-118">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> <dt>

<span data-ttu-id="fc9fd-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="fc9fd-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="fc9fd-120">As distâncias para o plano de recorte de profundidade mais distante.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-120">The distances to the farther depth clipping plane.</span></span> <span data-ttu-id="fc9fd-121">Essa distância será negativa se o plano estiver por trás do visualizador.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-121">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc9fd-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc9fd-122">Return value</span></span>

<span data-ttu-id="fc9fd-123">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fc9fd-124">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fc9fd-124">Error codes</span></span>

<span data-ttu-id="fc9fd-125">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9fd-125">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fc9fd-126">Nome</span><span class="sxs-lookup"><span data-stu-id="fc9fd-126">Name</span></span>                                                                                                  | <span data-ttu-id="fc9fd-127">Significado</span><span class="sxs-lookup"><span data-stu-id="fc9fd-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc9fd-128"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc9fd-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fc9fd-129">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fc9fd-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fc9fd-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc9fd-130">Remarks</span></span>

<span data-ttu-id="fc9fd-131">A função **glOrtho** descreve uma matriz de perspectiva que produz uma projeção paralela.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-131">The **glOrtho** function describes a perspective matrix that produces a parallel projection.</span></span> <span data-ttu-id="fc9fd-132">Os parâmetros (*esquerda*, *inferior*, *Near*) e (*direita*, *superior*, *Near*) especificam os pontos no plano de recorte próximo que são mapeados para os cantos inferior esquerdo e superior direito da janela, respectivamente, supondo que o olho está localizado em (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="fc9fd-132">The (*left*, *bottom*, *near*) and (*right*, *top*, *near*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0).</span></span> <span data-ttu-id="fc9fd-133">O parâmetro *far* especifica o local do plano de recorte distante.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-133">The *far* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="fc9fd-134">Tanto *zNear* como *zFar* podem ser positivos ou negativos.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-134">Both *zNear* and *zFar* can be either positive or negative.</span></span> <span data-ttu-id="fc9fd-135">A matriz correspondente é mostrada na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-135">The corresponding matrix is shown in the following image.</span></span>

![Diagrama mostrando a matriz de perspectiva que a função glOrtho descreve.](images/ortho1.png)

<span data-ttu-id="fc9fd-137">onde</span><span class="sxs-lookup"><span data-stu-id="fc9fd-137">where</span></span>

![Equações que descrevem a matriz de perspectiva.](images/ortho2.png)

<span data-ttu-id="fc9fd-139">A matriz atual é multiplicada por essa matriz com o resultado que substitui a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-139">The current matrix is multiplied by this matrix with the result replacing the current matrix.</span></span> <span data-ttu-id="fc9fd-140">Ou seja, se M for a matriz atual e O for a matriz Ortho, M será substituído por M O.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-140">That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M   O.</span></span>

<span data-ttu-id="fc9fd-141">Use [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** para salvar e restaurar a pilha de matriz atual.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-141">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the current matrix stack.</span></span> <span data-ttu-id="fc9fd-142">Use [**glMatrixMode**](glmatrixmode.md) para definir a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="fc9fd-142">Use [**glMatrixMode**](glmatrixmode.md) to set the current matrix.</span></span>

<span data-ttu-id="fc9fd-143">As funções a seguir recuperam informações relacionadas ao **glOrtho**:</span><span class="sxs-lookup"><span data-stu-id="fc9fd-143">The following functions retrieve information related to **glOrtho**:</span></span>

<span data-ttu-id="fc9fd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="fc9fd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="fc9fd-145">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="fc9fd-145">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="fc9fd-146"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="fc9fd-146">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="fc9fd-147">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="fc9fd-147">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="fc9fd-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc9fd-148">Requirements</span></span>



| <span data-ttu-id="fc9fd-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc9fd-149">Requirement</span></span> | <span data-ttu-id="fc9fd-150">Valor</span><span class="sxs-lookup"><span data-stu-id="fc9fd-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9fd-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc9fd-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fc9fd-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc9fd-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fc9fd-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc9fd-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fc9fd-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc9fd-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc9fd-155">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fc9fd-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc9fd-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc9fd-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fc9fd-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc9fd-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc9fd-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc9fd-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc9fd-159">DLL</span><span class="sxs-lookup"><span data-stu-id="fc9fd-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc9fd-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc9fd-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc9fd-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc9fd-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc9fd-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fc9fd-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fc9fd-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fc9fd-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fc9fd-164">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="fc9fd-164">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="fc9fd-165">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="fc9fd-165">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="fc9fd-166">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="fc9fd-166">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="fc9fd-167">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="fc9fd-167">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="fc9fd-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="fc9fd-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





