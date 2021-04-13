---
title: função glEnableClientState (GL. h)
description: As funções glEnableClientState e glDisableClientState habilitam e desabilitam matrizes, respectivamente. | função glEnableClientState (GL. h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- função glEnableClientState OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e333a51d4c1fe0a5ff11c717790e03aa6d054a09
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298313"
---
# <a name="glenableclientstate-function"></a><span data-ttu-id="9b53a-105">função glEnableClientState</span><span class="sxs-lookup"><span data-stu-id="9b53a-105">glEnableClientState function</span></span>

<span data-ttu-id="9b53a-106">As funções **glEnableClientState** e [**glDisableClientState**](gldisableclientstate.md) habilitam e desabilitam matrizes, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9b53a-106">The **glEnableClientState** and [**glDisableClientState**](gldisableclientstate.md) functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b53a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b53a-107">Syntax</span></span>


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="9b53a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b53a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b53a-109">*array*</span><span class="sxs-lookup"><span data-stu-id="9b53a-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="9b53a-110">Uma constante simbólica para a matriz que você deseja habilitar ou desabilitar.</span><span class="sxs-lookup"><span data-stu-id="9b53a-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="9b53a-111">Esse parâmetro pode assumir um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b53a-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="9b53a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="9b53a-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="9b53a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9b53a-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="9b53a-114"><dt>**\_matriz de cores GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="9b53a-115">Se habilitada, use matrizes de cores com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="9b53a-116">Consulte também [**glColorPointer**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="9b53a-117"><dt>**\_matriz do \_ sinalizador do Edge GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="9b53a-118">Se habilitada, use matrizes de sinalizador de borda com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="9b53a-119">Consulte também [**glEdgeFlagPointer**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="9b53a-120"><dt>**\_matriz de índice GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="9b53a-121">Se habilitada, use matrizes de índice com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="9b53a-122">Consulte também [**glIndexPointer**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="9b53a-123"><dt>**matriz do GL \_ normal \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="9b53a-124">Se habilitada, use matrizes normais com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="9b53a-125">Consulte também [**glNormalPointer**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="9b53a-126"><dt>**\_matriz GL \_ coord de textura \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="9b53a-127">Se habilitada, use matrizes de coordenadas de textura com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="9b53a-128">Consulte também [**glTexCoordPointer**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="9b53a-129"><dt>**\_matriz de vértice GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="9b53a-130">Se habilitada, use matrizes de vértice com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="9b53a-131">Consulte também [**glVertexPointer**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="9b53a-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b53a-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b53a-132">Return value</span></span>

<span data-ttu-id="9b53a-133">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9b53a-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9b53a-134">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9b53a-134">Error codes</span></span>

<span data-ttu-id="9b53a-135">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9b53a-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9b53a-136">Nome</span><span class="sxs-lookup"><span data-stu-id="9b53a-136">Name</span></span>                                                                                             | <span data-ttu-id="9b53a-137">Significado</span><span class="sxs-lookup"><span data-stu-id="9b53a-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9b53a-138"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="9b53a-139">a *matriz* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="9b53a-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9b53a-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b53a-140">Remarks</span></span>

<span data-ttu-id="9b53a-141">As funções **glEnableClientState** e **glDisableClientState** habilitam e desabilitam várias matrizes individuais.</span><span class="sxs-lookup"><span data-stu-id="9b53a-141">The **glEnableClientState** and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="9b53a-142">Use [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar a configuração atual de qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="9b53a-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="9b53a-143">Chamar **glEnableClientState** e **glDisableClientState** entre chamadas para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md) pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="9b53a-143">Calling **glEnableClientState** and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="9b53a-144">Se nenhum erro for gerado, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="9b53a-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="9b53a-145">As funções **glEnableClientState** e **glDisableClientState** só estão disponíveis no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9b53a-145">The **glEnableClientState** and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b53a-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b53a-146">Requirements</span></span>



| <span data-ttu-id="9b53a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b53a-147">Requirement</span></span> | <span data-ttu-id="9b53a-148">Valor</span><span class="sxs-lookup"><span data-stu-id="9b53a-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b53a-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b53a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9b53a-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9b53a-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9b53a-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b53a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9b53a-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9b53a-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b53a-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9b53a-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b53a-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9b53a-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b53a-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b53a-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b53a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9b53a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b53a-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b53a-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b53a-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b53a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b53a-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="9b53a-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="9b53a-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9b53a-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9b53a-162">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="9b53a-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="9b53a-163">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="9b53a-163">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="9b53a-164">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="9b53a-164">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="9b53a-165">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="9b53a-165">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="9b53a-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="9b53a-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="9b53a-167">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="9b53a-167">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9b53a-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9b53a-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9b53a-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="9b53a-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="9b53a-170">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="9b53a-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="9b53a-171">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="9b53a-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="9b53a-172">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="9b53a-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="9b53a-173">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="9b53a-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="9b53a-174">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="9b53a-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





