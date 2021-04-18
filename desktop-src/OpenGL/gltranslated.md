---
title: função glTranslated (GL. h)
description: A função glTranslated multiplica a matriz atual por uma matriz de conversão.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- função glTranslated OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105796389"
---
# <a name="gltranslated-function"></a><span data-ttu-id="20829-104">função glTranslated</span><span class="sxs-lookup"><span data-stu-id="20829-104">glTranslated function</span></span>

<span data-ttu-id="20829-105">A função **glTranslated** multiplica a matriz atual por uma matriz de conversão.</span><span class="sxs-lookup"><span data-stu-id="20829-105">The **glTranslated** function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="20829-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20829-106">Syntax</span></span>


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="20829-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20829-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20829-108">*x*</span><span class="sxs-lookup"><span data-stu-id="20829-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="20829-109">A coordenada *x* de um vetor de tradução.</span><span class="sxs-lookup"><span data-stu-id="20829-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="20829-110">*y*</span><span class="sxs-lookup"><span data-stu-id="20829-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="20829-111">A coordenada *y* de um vetor de tradução.</span><span class="sxs-lookup"><span data-stu-id="20829-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="20829-112">*z*</span><span class="sxs-lookup"><span data-stu-id="20829-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="20829-113">A coordenada *z* de um vetor de tradução.</span><span class="sxs-lookup"><span data-stu-id="20829-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20829-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20829-114">Return value</span></span>

<span data-ttu-id="20829-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="20829-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20829-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="20829-116">Remarks</span></span>

<span data-ttu-id="20829-117">A função **glTranslated** produz a tradução especificada por (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="20829-117">The **glTranslated** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="20829-118">O vetor de conversão é usado para calcular uma matriz de conversão 4x4:</span><span class="sxs-lookup"><span data-stu-id="20829-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Diagrama mostrando a matriz de tradução 4x4 especificada por x, y, z.](images/trans01.png)

<span data-ttu-id="20829-120">A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de tradução, com o produto que substitui a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="20829-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="20829-121">Ou seja, se M for a matriz atual e T for a matriz de conversão, M será substituído por M T.</span><span class="sxs-lookup"><span data-stu-id="20829-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="20829-122">Se o modo de matriz for uma \_ projeção GL MODELVIEW ou GL \_ , todos os objetos desenhados depois de **glTranslated** serão convertidos.</span><span class="sxs-lookup"><span data-stu-id="20829-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslated** is called are translated.</span></span> <span data-ttu-id="20829-123">Use [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** para salvar e restaurar o sistema de coordenadas não traduzido.</span><span class="sxs-lookup"><span data-stu-id="20829-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="20829-124">As funções a seguir recuperam informações relacionadas ao [**glTranslated**](gltranslate.md):</span><span class="sxs-lookup"><span data-stu-id="20829-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md):</span></span>

<span data-ttu-id="20829-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="20829-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="20829-126">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="20829-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="20829-127"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="20829-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="20829-128">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="20829-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="20829-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20829-129">Requirements</span></span>



| <span data-ttu-id="20829-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="20829-130">Requirement</span></span> | <span data-ttu-id="20829-131">Valor</span><span class="sxs-lookup"><span data-stu-id="20829-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20829-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20829-132">Minimum supported client</span></span><br/> | <span data-ttu-id="20829-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20829-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="20829-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20829-134">Minimum supported server</span></span><br/> | <span data-ttu-id="20829-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20829-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20829-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20829-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="20829-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="20829-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="20829-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20829-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="20829-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20829-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="20829-140">DLL</span><span class="sxs-lookup"><span data-stu-id="20829-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20829-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20829-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20829-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="20829-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20829-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="20829-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="20829-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="20829-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="20829-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="20829-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="20829-146">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="20829-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="20829-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="20829-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="20829-148">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="20829-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="20829-149">**glScale**</span><span class="sxs-lookup"><span data-stu-id="20829-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





