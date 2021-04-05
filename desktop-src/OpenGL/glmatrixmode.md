---
title: função glMatrixMode (GL. h)
description: A função glMatrixMode especifica qual matriz é a matriz atual.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- função glMatrixMode OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085889"
---
# <a name="glmatrixmode-function"></a><span data-ttu-id="210da-104">função glMatrixMode</span><span class="sxs-lookup"><span data-stu-id="210da-104">glMatrixMode function</span></span>

<span data-ttu-id="210da-105">A função **glMatrixMode** especifica qual matriz é a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="210da-105">The **glMatrixMode** function specifies which matrix is the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="210da-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="210da-106">Syntax</span></span>


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="210da-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="210da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="210da-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="210da-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="210da-109">A pilha de matriz que é o destino para operações de matriz subsequentes.</span><span class="sxs-lookup"><span data-stu-id="210da-109">The matrix stack that is the target for subsequent matrix operations.</span></span> <span data-ttu-id="210da-110">O parâmetro *Mode* pode assumir um dos três valores.</span><span class="sxs-lookup"><span data-stu-id="210da-110">The *mode* parameter can assume one of three values.</span></span>



| <span data-ttu-id="210da-111">Valor</span><span class="sxs-lookup"><span data-stu-id="210da-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="210da-112">Significado</span><span class="sxs-lookup"><span data-stu-id="210da-112">Meaning</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <span data-ttu-id="210da-113"><dt>**\_MODELVIEW GL**</dt></span><span class="sxs-lookup"><span data-stu-id="210da-113"><dt>**GL\_MODELVIEW**</dt></span></span> </dl>    | <span data-ttu-id="210da-114">Aplica operações de matriz subsequentes à pilha de matriz modelview.</span><span class="sxs-lookup"><span data-stu-id="210da-114">Applies subsequent matrix operations to the modelview matrix stack.</span></span><br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <span data-ttu-id="210da-115"><dt>**\_projeção GL**</dt></span><span class="sxs-lookup"><span data-stu-id="210da-115"><dt>**GL\_PROJECTION**</dt></span></span> </dl> | <span data-ttu-id="210da-116">Aplica operações de matriz subsequentes à pilha de matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="210da-116">Applies subsequent matrix operations to the projection matrix stack.</span></span><br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <span data-ttu-id="210da-117"><dt>**\_textura GL**</dt></span><span class="sxs-lookup"><span data-stu-id="210da-117"><dt>**GL\_TEXTURE**</dt></span></span> </dl>          | <span data-ttu-id="210da-118">Aplica operações de matriz subsequentes à pilha de matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="210da-118">Applies subsequent matrix operations to the texture matrix stack.</span></span><br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="210da-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="210da-119">Return value</span></span>

<span data-ttu-id="210da-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="210da-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="210da-121">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="210da-121">Error codes</span></span>

<span data-ttu-id="210da-122">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="210da-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="210da-123">Nome</span><span class="sxs-lookup"><span data-stu-id="210da-123">Name</span></span>                                                                                                  | <span data-ttu-id="210da-124">Significado</span><span class="sxs-lookup"><span data-stu-id="210da-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="210da-125"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="210da-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="210da-126">o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="210da-126">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="210da-127"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="210da-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="210da-128">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="210da-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="210da-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="210da-129">Remarks</span></span>

<span data-ttu-id="210da-130">A função **glMatrixMode** define o modo de matriz atual.</span><span class="sxs-lookup"><span data-stu-id="210da-130">The **glMatrixMode** function sets the current matrix mode.</span></span>

<span data-ttu-id="210da-131">A função a seguir recupera informações relacionadas a **glMatrixMode**:</span><span class="sxs-lookup"><span data-stu-id="210da-131">The following function retrieves information related to **glMatrixMode**:</span></span>

<span data-ttu-id="210da-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="210da-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="210da-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="210da-133">Requirements</span></span>



| <span data-ttu-id="210da-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="210da-134">Requirement</span></span> | <span data-ttu-id="210da-135">Valor</span><span class="sxs-lookup"><span data-stu-id="210da-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="210da-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="210da-136">Minimum supported client</span></span><br/> | <span data-ttu-id="210da-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="210da-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="210da-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="210da-138">Minimum supported server</span></span><br/> | <span data-ttu-id="210da-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="210da-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="210da-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="210da-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="210da-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="210da-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="210da-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="210da-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="210da-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="210da-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="210da-144">DLL</span><span class="sxs-lookup"><span data-stu-id="210da-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="210da-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="210da-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="210da-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="210da-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210da-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="210da-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="210da-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="210da-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="210da-149">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="210da-149">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="210da-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="210da-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





