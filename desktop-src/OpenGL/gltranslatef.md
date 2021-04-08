---
title: função glTranslatef (GL. h)
description: A função glTranslatef multiplica a matriz atual por uma matriz de conversão.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- função glTranslatef OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b52c3890b70ecb931211af1788afe2b8e6ad4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103837574"
---
# <a name="gltranslatef-function"></a><span data-ttu-id="e6440-104">função glTranslatef</span><span class="sxs-lookup"><span data-stu-id="e6440-104">glTranslatef function</span></span>

<span data-ttu-id="e6440-105">A função [**glTranslatef**](gltranslate.md) multiplica a matriz atual por uma matriz de conversão.</span><span class="sxs-lookup"><span data-stu-id="e6440-105">The [**glTranslatef**](gltranslate.md) function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6440-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6440-106">Syntax</span></span>


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="e6440-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6440-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6440-108">*x*</span><span class="sxs-lookup"><span data-stu-id="e6440-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="e6440-109">A coordenada *x* de um vetor de tradução.</span><span class="sxs-lookup"><span data-stu-id="e6440-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="e6440-110">*y*</span><span class="sxs-lookup"><span data-stu-id="e6440-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="e6440-111">A coordenada *y* de um vetor de tradução.</span><span class="sxs-lookup"><span data-stu-id="e6440-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="e6440-112">*z*</span><span class="sxs-lookup"><span data-stu-id="e6440-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="e6440-113">A coordenada *z* de um vetor de tradução.</span><span class="sxs-lookup"><span data-stu-id="e6440-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6440-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6440-114">Return value</span></span>

<span data-ttu-id="e6440-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e6440-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6440-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6440-116">Remarks</span></span>

<span data-ttu-id="e6440-117">A função **glTranslatef** produz a tradução especificada por (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="e6440-117">The **glTranslatef** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="e6440-118">O vetor de conversão é usado para calcular uma matriz de conversão 4x4:</span><span class="sxs-lookup"><span data-stu-id="e6440-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Diagrama mostrando a matriz de tradução 4x4 especificada por x, y, z.](images/trans01.png)

<span data-ttu-id="e6440-120">A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de tradução, com o produto que substitui a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="e6440-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="e6440-121">Ou seja, se M for a matriz atual e T for a matriz de conversão, M será substituído por M T.</span><span class="sxs-lookup"><span data-stu-id="e6440-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="e6440-122">Se o modo de matriz for uma \_ projeção GL MODELVIEW ou GL \_ , todos os objetos desenhados depois de **glTranslatef** serão convertidos.</span><span class="sxs-lookup"><span data-stu-id="e6440-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslatef** is called are translated.</span></span> <span data-ttu-id="e6440-123">Use [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** para salvar e restaurar o sistema de coordenadas não traduzido.</span><span class="sxs-lookup"><span data-stu-id="e6440-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="e6440-124">As funções a seguir recuperam informações relacionadas a [**glTranslated**](gltranslate.md) e **glTranslatef**:</span><span class="sxs-lookup"><span data-stu-id="e6440-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md) and **glTranslatef**:</span></span>

<span data-ttu-id="e6440-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="e6440-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="e6440-126">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="e6440-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="e6440-127"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e6440-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="e6440-128">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e6440-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="e6440-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6440-129">Requirements</span></span>



| <span data-ttu-id="e6440-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6440-130">Requirement</span></span> | <span data-ttu-id="e6440-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e6440-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6440-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6440-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e6440-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6440-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e6440-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6440-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e6440-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6440-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6440-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6440-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6440-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6440-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e6440-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6440-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6440-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6440-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6440-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e6440-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6440-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6440-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6440-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6440-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6440-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e6440-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e6440-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e6440-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e6440-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="e6440-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="e6440-146">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e6440-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e6440-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="e6440-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="e6440-148">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="e6440-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="e6440-149">**glScale**</span><span class="sxs-lookup"><span data-stu-id="e6440-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





