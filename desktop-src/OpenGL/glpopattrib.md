---
title: função glPopAttrib (GL. h)
description: Exibe a pilha de atributos.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- função glPopAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771834"
---
# <a name="glpopattrib-function"></a><span data-ttu-id="876ea-104">função glPopAttrib</span><span class="sxs-lookup"><span data-stu-id="876ea-104">glPopAttrib function</span></span>

<span data-ttu-id="876ea-105">Exibe a pilha de atributos.</span><span class="sxs-lookup"><span data-stu-id="876ea-105">Pops the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="876ea-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="876ea-106">Syntax</span></span>


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="876ea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="876ea-107">Parameters</span></span>

<span data-ttu-id="876ea-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="876ea-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="876ea-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="876ea-109">Return value</span></span>

<span data-ttu-id="876ea-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="876ea-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="876ea-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="876ea-111">Error codes</span></span>

<span data-ttu-id="876ea-112">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="876ea-112">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="876ea-113">Nome</span><span class="sxs-lookup"><span data-stu-id="876ea-113">Name</span></span>                                                                                                  | <span data-ttu-id="876ea-114">Significado</span><span class="sxs-lookup"><span data-stu-id="876ea-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="876ea-115"><dt>**\_estouro negativo de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="876ea-115"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="876ea-116">A função foi chamada enquanto a pilha de atributos estava vazia.</span><span class="sxs-lookup"><span data-stu-id="876ea-116">The function was called while the attribute stack was empty.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="876ea-117"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="876ea-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="876ea-118">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="876ea-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="876ea-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="876ea-119">Remarks</span></span>

<span data-ttu-id="876ea-120">A função [**glPushAttrib**](glpushattrib.md) usa um argumento, uma máscara que indica quais grupos de variáveis de estado salvar na pilha de atributos.</span><span class="sxs-lookup"><span data-stu-id="876ea-120">The [**glPushAttrib**](glpushattrib.md) function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="876ea-121">As constantes simbólicas são usadas para definir os bits na máscara.</span><span class="sxs-lookup"><span data-stu-id="876ea-121">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="876ea-122">O parâmetro Mask normalmente é construído por **ou** em várias dessas constantes juntas.</span><span class="sxs-lookup"><span data-stu-id="876ea-122">The mask parameter is typically constructed by **OR** ing several of these constants together.</span></span> <span data-ttu-id="876ea-123">A máscara especial GL \_ todos \_ os \_ bits de Atrib. pode ser usada para salvar todos os Estados empilháveis.</span><span class="sxs-lookup"><span data-stu-id="876ea-123">The special mask GL\_ALL\_ATTRIB\_BITS can be used to save all stackable states.</span></span>

<span data-ttu-id="876ea-124">A função **glPopAttrib** restaura os valores das variáveis de estado salvas com o último comando [**glPushAttrib**](glpushattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="876ea-124">The **glPopAttrib** function restores the values of the state variables saved with the last [**glPushAttrib**](glpushattrib.md) command.</span></span> <span data-ttu-id="876ea-125">Aqueles não salvos são deixados inalterados.</span><span class="sxs-lookup"><span data-stu-id="876ea-125">Those not saved are left unchanged.</span></span>

<span data-ttu-id="876ea-126">É um erro enviar atributos por push para uma pilha completa ou para os atributos pop de uma pilha vazia.</span><span class="sxs-lookup"><span data-stu-id="876ea-126">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="876ea-127">Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.</span><span class="sxs-lookup"><span data-stu-id="876ea-127">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="876ea-128">Inicialmente, a pilha de atributos está vazia.</span><span class="sxs-lookup"><span data-stu-id="876ea-128">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="876ea-129">Nem todos os valores para o estado OpenGL podem ser salvos na pilha de atributos.</span><span class="sxs-lookup"><span data-stu-id="876ea-129">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="876ea-130">Por exemplo, o pacote de pixel e o estado de desempacotamento, estado do modo de renderização e estado de comentários e de seleção não podem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="876ea-130">For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.</span></span>

<span data-ttu-id="876ea-131">A profundidade da pilha de atributos depende da implementação, mas deve ser pelo menos 16.</span><span class="sxs-lookup"><span data-stu-id="876ea-131">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="876ea-132">As funções a seguir recuperam informações relacionadas a [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**:</span><span class="sxs-lookup"><span data-stu-id="876ea-132">The following functions retrieve information related to [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**:</span></span>

<span data-ttu-id="876ea-133">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) profundidade de pilha de Atrib glGet com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="876ea-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="876ea-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ profundidade máxima de pilha de \_ ATRIB \_ glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="876ea-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="876ea-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="876ea-135">Requirements</span></span>



| <span data-ttu-id="876ea-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="876ea-136">Requirement</span></span> | <span data-ttu-id="876ea-137">Valor</span><span class="sxs-lookup"><span data-stu-id="876ea-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="876ea-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="876ea-138">Minimum supported client</span></span><br/> | <span data-ttu-id="876ea-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="876ea-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="876ea-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="876ea-140">Minimum supported server</span></span><br/> | <span data-ttu-id="876ea-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="876ea-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="876ea-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="876ea-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="876ea-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="876ea-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="876ea-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="876ea-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="876ea-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="876ea-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="876ea-146">DLL</span><span class="sxs-lookup"><span data-stu-id="876ea-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="876ea-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="876ea-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="876ea-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="876ea-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876ea-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="876ea-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="876ea-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="876ea-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="876ea-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="876ea-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="876ea-152">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="876ea-152">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="876ea-153">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="876ea-153">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="876ea-154">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="876ea-154">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="876ea-155">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="876ea-155">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="876ea-156">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="876ea-156">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="876ea-157">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="876ea-157">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="876ea-158">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="876ea-158">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="876ea-159">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="876ea-159">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="876ea-160">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="876ea-160">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="876ea-161">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="876ea-161">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="876ea-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="876ea-162">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="876ea-163">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="876ea-163">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="876ea-164">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="876ea-164">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="876ea-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="876ea-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





