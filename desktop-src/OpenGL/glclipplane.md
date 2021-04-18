---
title: função glClipPlane (GL. h)
description: A função glClipPlane especifica um plano no qual toda a geometria é recortada.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- função glClipPlane OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760222"
---
# <a name="glclipplane-function"></a><span data-ttu-id="d0a16-104">função glClipPlane</span><span class="sxs-lookup"><span data-stu-id="d0a16-104">glClipPlane function</span></span>

<span data-ttu-id="d0a16-105">A função **glClipPlane** especifica um plano no qual toda a geometria é recortada.</span><span class="sxs-lookup"><span data-stu-id="d0a16-105">The **glClipPlane** function specifies a plane against which all geometry is clipped.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0a16-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0a16-106">Syntax</span></span>


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="d0a16-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0a16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a16-108">*aérea*</span><span class="sxs-lookup"><span data-stu-id="d0a16-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a16-109">O plano de recorte que está sendo posicionado.</span><span class="sxs-lookup"><span data-stu-id="d0a16-109">The clipping plane that is being positioned.</span></span> <span data-ttu-id="d0a16-110">Os nomes simbólicos da forma GL o \_ clip do \_ plano *i*, onde *eu* é um inteiro entre 0 e GL o \_ máximo \_ de recortes \_ de clipe-1, são aceitos.</span><span class="sxs-lookup"><span data-stu-id="d0a16-110">Symbolic names of the form GL\_CLIP\_PLANE *i*, where *i* is an integer between 0 and GL\_MAX\_CLIP\_PLANES - 1, are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d0a16-111">*subscrito*</span><span class="sxs-lookup"><span data-stu-id="d0a16-111">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a16-112">O endereço de uma matriz de quatro valores de ponto flutuante de precisão dupla.</span><span class="sxs-lookup"><span data-stu-id="d0a16-112">The address of an array of four double-precision floating-point values.</span></span> <span data-ttu-id="d0a16-113">Esses valores são interpretados como uma equação de plano.</span><span class="sxs-lookup"><span data-stu-id="d0a16-113">These values are interpreted as a plane equation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a16-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0a16-114">Return value</span></span>

<span data-ttu-id="d0a16-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d0a16-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d0a16-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d0a16-116">Error codes</span></span>

<span data-ttu-id="d0a16-117">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d0a16-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d0a16-118">Nome</span><span class="sxs-lookup"><span data-stu-id="d0a16-118">Name</span></span>                                                                                                  | <span data-ttu-id="d0a16-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d0a16-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d0a16-120"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a16-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d0a16-121">o *plano* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="d0a16-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="d0a16-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a16-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d0a16-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d0a16-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d0a16-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0a16-124">Remarks</span></span>

<span data-ttu-id="d0a16-125">A geometria é sempre recortada em relação aos limites de um frustum de seis planos em *x*, *y* e *z*.</span><span class="sxs-lookup"><span data-stu-id="d0a16-125">Geometry is always clipped against the boundaries of a six-plane frustum in *x*, *y*, and *z*.</span></span> <span data-ttu-id="d0a16-126">A função **glClipPlane** permite a especificação de planos adicionais, não necessariamente perpendicular ao eixo *x*, eixo *y* ou eixo *z*, em relação ao qual toda a geometria é recortada.</span><span class="sxs-lookup"><span data-stu-id="d0a16-126">The **glClipPlane** function allows the specification of additional planes, not necessarily perpendicular to the *x-* axis, *y-* axis, or *z*-axis, against which all geometry is clipped.</span></span> <span data-ttu-id="d0a16-127">Até o GL \_ máximo \_ , os planos de planos de corte \_ podem ser especificados, onde o GL \_ Max \_ recortes \_ é pelo menos seis em todas as implementações.</span><span class="sxs-lookup"><span data-stu-id="d0a16-127">Up to GL\_MAX\_CLIP\_PLANES planes can be specified, where GL\_MAX\_CLIP\_PLANES is at least six in all implementations.</span></span> <span data-ttu-id="d0a16-128">Como a região de recorte resultante é a interseção dos espaços de meia definição, ela é sempre convexa.</span><span class="sxs-lookup"><span data-stu-id="d0a16-128">Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.</span></span>

<span data-ttu-id="d0a16-129">A função **glClipPlane** especifica um meio-espaço usando uma equação de plano de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="d0a16-129">The **glClipPlane** function specifies a half-space using a four-component plane equation.</span></span> <span data-ttu-id="d0a16-130">Quando você chama **glClipPlane**, a *equação* é transformada pelo inverso da matriz modelview e armazenada nas coordenadas de olho resultante.</span><span class="sxs-lookup"><span data-stu-id="d0a16-130">When you call **glClipPlane**,*equation* is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates.</span></span> <span data-ttu-id="d0a16-131">As alterações subsequentes na matriz modelview não têm efeito sobre os componentes de equação de plano armazenado.</span><span class="sxs-lookup"><span data-stu-id="d0a16-131">Subsequent changes to the modelview matrix have no effect on the stored plane-equation components.</span></span> <span data-ttu-id="d0a16-132">Se o produto de ponto das coordenadas de olho de um vértice com os componentes da equação do plano armazenado for positivo ou zero, o vértice estará em relação a esse plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="d0a16-132">If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane.</span></span> <span data-ttu-id="d0a16-133">Caso contrário, ele está fora.</span><span class="sxs-lookup"><span data-stu-id="d0a16-133">Otherwise, it is out.</span></span>

<span data-ttu-id="d0a16-134">Use as funções [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) para habilitar e desabilitar planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="d0a16-134">Use the [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions to enable and disable clipping planes.</span></span> <span data-ttu-id="d0a16-135">Chame os planos de recorte com o argumento GL de \_ clipe \_ *i*, onde é o número do plano. </span><span class="sxs-lookup"><span data-stu-id="d0a16-135">Call clipping planes with the argument GL\_CLIP\_PLANE *i*, where *i* is the plane number.</span></span>

<span data-ttu-id="d0a16-136">Por padrão, todos os planos de recorte são definidos como (0, 0, 0, 0) em coordenadas de olho e estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d0a16-136">By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.</span></span>

<span data-ttu-id="d0a16-137">É sempre o caso que o GL \_ clip \_ avião *i* = GL \_ clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="d0a16-137">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="d0a16-138">As funções a seguir recuperam informações relacionadas ao **glClipPlane**:</span><span class="sxs-lookup"><span data-stu-id="d0a16-138">The following functions retrieve information related to **glClipPlane**:</span></span>

[<span data-ttu-id="d0a16-139">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="d0a16-139">**glGetClipPlane**</span></span>](glgetclipplane.md)

<span data-ttu-id="d0a16-140">[**glIsEnabled**](glisenabled.md) com Argument GL \_ clip \_ avião *i*</span><span class="sxs-lookup"><span data-stu-id="d0a16-140">[**glIsEnabled**](glisenabled.md) with argument GL\_CLIP\_PLANE *i*</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a16-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0a16-141">Requirements</span></span>



| <span data-ttu-id="d0a16-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a16-142">Requirement</span></span> | <span data-ttu-id="d0a16-143">Valor</span><span class="sxs-lookup"><span data-stu-id="d0a16-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a16-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0a16-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a16-145">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d0a16-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d0a16-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0a16-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a16-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d0a16-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0a16-148">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d0a16-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a16-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a16-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d0a16-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0a16-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0a16-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0a16-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0a16-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d0a16-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0a16-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0a16-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a16-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0a16-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a16-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d0a16-155">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d0a16-156">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="d0a16-156">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="d0a16-157">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="d0a16-157">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="d0a16-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d0a16-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d0a16-159">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="d0a16-159">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="d0a16-160">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d0a16-160">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





