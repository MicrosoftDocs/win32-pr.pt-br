---
title: função glGetClipPlane (GL. h)
description: A função glGetClipPlane retorna os coeficientes do plano de recorte especificado.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- função glGetClipPlane OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761407"
---
# <a name="glgetclipplane-function"></a><span data-ttu-id="bf7f4-104">função glGetClipPlane</span><span class="sxs-lookup"><span data-stu-id="bf7f4-104">glGetClipPlane function</span></span>

<span data-ttu-id="bf7f4-105">A função **glGetClipPlane** retorna os coeficientes do plano de recorte especificado.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-105">The **glGetClipPlane** function returns the coefficients of the specified clipping plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7f4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf7f4-106">Syntax</span></span>


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="bf7f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf7f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7f4-108">*aérea*</span><span class="sxs-lookup"><span data-stu-id="bf7f4-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="bf7f4-109">Um plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-109">A clipping plane.</span></span> <span data-ttu-id="bf7f4-110">O número de planos de recorte depende da implementação, mas há suporte para pelo menos seis planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-110">The number of clipping planes depends on the implementation, but at least six clipping planes are supported.</span></span> <span data-ttu-id="bf7f4-111">Elas são identificadas por nomes simbólicos do formulário GL de \_ clipe \_ *i,* em que 0 = *i* < GL \_ Max \_ recortes \_ .</span><span class="sxs-lookup"><span data-stu-id="bf7f4-111">They are identified by symbolic names of the form GL\_CLIP\_PLANE *i* where 0 = *i* < GL\_MAX\_CLIP\_PLANES.</span></span>

</dd> <dt>

<span data-ttu-id="bf7f4-112">*subscrito*</span><span class="sxs-lookup"><span data-stu-id="bf7f4-112">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="bf7f4-113">Retorna quatro valores de precisão dupla que são os coeficientes da equação de plano do *plano* em coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-113">Returns four double-precision values that are the coefficients of the plane equation of *plane* in eye coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7f4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf7f4-114">Return value</span></span>

<span data-ttu-id="bf7f4-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf7f4-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bf7f4-116">Error codes</span></span>

<span data-ttu-id="bf7f4-117">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7f4-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bf7f4-118">Nome</span><span class="sxs-lookup"><span data-stu-id="bf7f4-118">Name</span></span>                                                                                                  | <span data-ttu-id="bf7f4-119">Significado</span><span class="sxs-lookup"><span data-stu-id="bf7f4-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf7f4-120"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7f4-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bf7f4-121">o *plano* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="bf7f4-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7f4-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bf7f4-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bf7f4-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bf7f4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf7f4-124">Remarks</span></span>

<span data-ttu-id="bf7f4-125">A função **glGetClipPlane** retorna na *equação* os quatro coeficientes da equação de plano para o *plano*.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-125">The **glGetClipPlane** function returns in *equation* the four coefficients of the plane equation for *plane*.</span></span>

<span data-ttu-id="bf7f4-126">É sempre o caso que o GL \_ clip \_ avião *i* = GL \_ clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-126">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="bf7f4-127">Se um erro for gerado, nenhuma alteração será feita no conteúdo da *equação*.</span><span class="sxs-lookup"><span data-stu-id="bf7f4-127">If an error is generated, no change is made to the contents of *equation*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7f4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf7f4-128">Requirements</span></span>



| <span data-ttu-id="bf7f4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf7f4-129">Requirement</span></span> | <span data-ttu-id="bf7f4-130">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7f4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7f4-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf7f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7f4-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bf7f4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf7f4-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf7f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7f4-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bf7f4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf7f4-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bf7f4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7f4-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7f4-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bf7f4-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf7f4-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf7f4-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf7f4-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf7f4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7f4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf7f4-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf7f4-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7f4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf7f4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7f4-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bf7f4-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bf7f4-143">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="bf7f4-143">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="bf7f4-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bf7f4-144">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





