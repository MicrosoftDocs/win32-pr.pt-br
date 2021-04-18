---
title: função glEvalCoord1dv (GL. h)
description: A função glEvalCoord1dv avalia mapas unidimensionais habilitados.
ms.assetid: 6f966141-d4e6-4b54-b465-3ced33b57caf
keywords:
- função glEvalCoord1dv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018c984c74ed6fa0d7224e7e0520c023e8b6bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753158"
---
# <a name="glevalcoord1dv-function"></a><span data-ttu-id="5e5d5-104">função glEvalCoord1dv</span><span class="sxs-lookup"><span data-stu-id="5e5d5-104">glEvalCoord1dv function</span></span>

<span data-ttu-id="5e5d5-105">A função [**glEvalCoord1dv**](glevalcoord1d.md) avalia mapas unidimensionais habilitados.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-105">The [**glEvalCoord1dv**](glevalcoord1d.md) function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5d5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e5d5-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1dv(
   const GLdouble *u
);
```



## <a name="parameters"></a><span data-ttu-id="5e5d5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e5d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5d5-108">*u*</span><span class="sxs-lookup"><span data-stu-id="5e5d5-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="5e5d5-109">Um ponteiro para uma matriz que contém a coordenada de domínio *u*.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5d5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e5d5-110">Return value</span></span>

<span data-ttu-id="5e5d5-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e5d5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e5d5-112">Remarks</span></span>

<span data-ttu-id="5e5d5-113">A função **glEvalCoord1dv** avalia os mapas unidimensionais habilitados no argumento *u*.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-113">The **glEvalCoord1dv** function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="5e5d5-114">Defina mapas com [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="5e5d5-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="5e5d5-115">Habilite ou desabilite-os com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="5e5d5-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="5e5d5-116">Quando uma das funções **glEvalCoord** é emitida, todos os mapas atualmente habilitados da dimensão indicada são avaliados.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="5e5d5-117">Em seguida, para cada mapa habilitado, é como se a função OpenGL correspondente fosse emitida com o valor calculado.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="5e5d5-118">Ou seja, se \_ \_ o índice GL MAP1 index ou GL \_ map2 \_ estiver habilitado, uma função [**glIndex**](glindex-functions.md) será simulada.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="5e5d5-119">Se GL \_ MAP1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 estiver habilitado, uma função **glColor** será simulada.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="5e5d5-120">Se GL \_ MAP1 \_ normal ou GL \_ map2 \_ normal estiver habilitado, um vetor normal é produzido e, se qualquer uma das \_ MAP1 de \_ textura GL \_ coord \_ 1, GL \_ MAP1 \_ Texture \_ coord \_ 2, GL \_ MAP1 de textura coord \_ \_ \_ 3, GL \_ MAP1 de \_ textura \_ coord \_ 4, GL map2 de textura coord \_ \_ \_ \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL map2 de textura \_ \_ \_ coord \_ 3 e GL \_ map2 Texture coord \_ \_ \_ 4 estiver habilitado, uma função [**glTexCoord**](gltexcoord-functions.md) apropriada será simulada.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="5e5d5-121">O OpenGL usa valores avaliados em vez de valores atuais para as avaliações habilitadas e valores atuais de outra forma, para as coordenadas de cor, índice de cor, normal e textura.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="5e5d5-122">No entanto, os valores avaliados não atualizam os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="5e5d5-123">Portanto, se as funções [**glVertex**](glvertex-functions.md) estiverem intercaladas com as funções **glEvalCoord** , as coordenadas Color, normal e Texture associadas às funções **glVertex** não serão afetadas pelos valores gerados pelas funções **glEvalCoord** , mas somente pelas funções [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) mais recentes.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="5e5d5-124">As funções a seguir recuperam informações relacionadas à função **glEvalCoord1dv** :</span><span class="sxs-lookup"><span data-stu-id="5e5d5-124">The following functions retrieve information related to the **glEvalCoord1dv** function:</span></span>

<span data-ttu-id="5e5d5-125">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 3</span><span class="sxs-lookup"><span data-stu-id="5e5d5-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="5e5d5-126">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="5e5d5-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="5e5d5-127">índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_</span><span class="sxs-lookup"><span data-stu-id="5e5d5-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="5e5d5-128">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="5e5d5-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="5e5d5-129">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="5e5d5-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="5e5d5-130">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="5e5d5-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="5e5d5-131">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="5e5d5-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="5e5d5-132">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="5e5d5-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="5e5d5-133">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="5e5d5-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="5e5d5-134">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 3</span><span class="sxs-lookup"><span data-stu-id="5e5d5-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="5e5d5-135">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="5e5d5-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="5e5d5-136">índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_</span><span class="sxs-lookup"><span data-stu-id="5e5d5-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="5e5d5-137">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="5e5d5-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="5e5d5-138">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="5e5d5-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="5e5d5-139">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="5e5d5-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="5e5d5-140">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="5e5d5-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="5e5d5-141">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="5e5d5-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="5e5d5-142">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="5e5d5-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="5e5d5-143">[**glIsEnabled**](glisenabled.md) com Argument GL \_ automático \_ normal</span><span class="sxs-lookup"><span data-stu-id="5e5d5-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5d5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e5d5-144">Requirements</span></span>



| <span data-ttu-id="5e5d5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e5d5-145">Requirement</span></span> | <span data-ttu-id="5e5d5-146">Valor</span><span class="sxs-lookup"><span data-stu-id="5e5d5-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5d5-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5d5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5d5-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e5d5-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5e5d5-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5d5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5d5-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e5d5-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e5d5-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5e5d5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e5d5-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e5d5-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5e5d5-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e5d5-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e5d5-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e5d5-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e5d5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="5e5d5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5d5-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e5d5-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e5d5-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e5d5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5d5-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-159">**glColor**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-160">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-163">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-165">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-166">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-170">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-171">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-172">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="5e5d5-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





