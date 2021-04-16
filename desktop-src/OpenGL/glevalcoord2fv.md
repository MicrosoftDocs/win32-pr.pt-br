---
title: função glEvalCoord2fv (GL. h)
description: A função glEvalCoord2fv avalia os mapas bidimensionais habilitados.
ms.assetid: fff786b4-a9e1-4f3e-a62e-36e89bc9c35d
keywords:
- função glEvalCoord2fv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e277b0b71361588f8a9835ec3b8891b49f9482a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104550264"
---
# <a name="glevalcoord2fv-function"></a><span data-ttu-id="c051c-104">função glEvalCoord2fv</span><span class="sxs-lookup"><span data-stu-id="c051c-104">glEvalCoord2fv function</span></span>

<span data-ttu-id="c051c-105">A função **glEvalCoord2fv** avalia os mapas bidimensionais habilitados.</span><span class="sxs-lookup"><span data-stu-id="c051c-105">The **glEvalCoord2fv** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="c051c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c051c-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2fv(
   const GLfloat *u
);
```



## <a name="parameters"></a><span data-ttu-id="c051c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c051c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c051c-108">*u*</span><span class="sxs-lookup"><span data-stu-id="c051c-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="c051c-109">Um ponteiro para uma matriz que contém a coordenada de domínio *u*.</span><span class="sxs-lookup"><span data-stu-id="c051c-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c051c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c051c-110">Return value</span></span>

<span data-ttu-id="c051c-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c051c-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c051c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c051c-112">Remarks</span></span>

<span data-ttu-id="c051c-113">A função **glEvalCoord2fv** avalia os mapas bidimensionais habilitados usando dois valores de domínio, *u* e *v*.</span><span class="sxs-lookup"><span data-stu-id="c051c-113">The **glEvalCoord2fv** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="c051c-114">Defina mapas com [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="c051c-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="c051c-115">Habilite ou desabilite-os com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="c051c-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="c051c-116">Quando uma das funções **glEvalCoord** é emitida, todos os mapas atualmente habilitados da dimensão indicada são avaliados.</span><span class="sxs-lookup"><span data-stu-id="c051c-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="c051c-117">Em seguida, para cada mapa habilitado, é como se a função OpenGL correspondente fosse emitida com o valor calculado.</span><span class="sxs-lookup"><span data-stu-id="c051c-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="c051c-118">Ou seja, se \_ \_ o índice GL MAP1 index ou GL \_ map2 \_ estiver habilitado, uma função [**glIndex**](glindex-functions.md) será simulada.</span><span class="sxs-lookup"><span data-stu-id="c051c-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="c051c-119">Se GL \_ MAP1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 estiver habilitado, uma função **glColor** será simulada.</span><span class="sxs-lookup"><span data-stu-id="c051c-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="c051c-120">Se GL \_ MAP1 \_ normal ou GL \_ map2 \_ normal estiver habilitado, um vetor normal é produzido e, se qualquer uma das \_ MAP1 de \_ textura GL \_ coord \_ 1, GL \_ MAP1 \_ Texture \_ coord \_ 2, GL \_ MAP1 de textura coord \_ \_ \_ 3, GL \_ MAP1 de \_ textura \_ coord \_ 4, GL map2 de textura coord \_ \_ \_ \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL map2 de textura \_ \_ \_ coord \_ 3 e GL \_ map2 Texture coord \_ \_ \_ 4 estiver habilitado, uma função [**glTexCoord**](gltexcoord-functions.md) apropriada será simulada.</span><span class="sxs-lookup"><span data-stu-id="c051c-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="c051c-121">O OpenGL usa valores avaliados em vez de valores atuais para as avaliações habilitadas e valores atuais de outra forma, para as coordenadas de cor, índice de cor, normal e textura.</span><span class="sxs-lookup"><span data-stu-id="c051c-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="c051c-122">No entanto, os valores avaliados não atualizam os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="c051c-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="c051c-123">Portanto, se as funções [**glVertex**](glvertex-functions.md) estiverem intercaladas com as funções **glEvalCoord** , as coordenadas Color, normal e Texture associadas às funções **glVertex** não serão afetadas pelos valores gerados pelas funções **glEvalCoord** , mas somente pelas funções [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) mais recentes.</span><span class="sxs-lookup"><span data-stu-id="c051c-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="c051c-124">Se a geração normal automática estiver habilitada, **glEvalCoord2fv** chamará [**glEnable**](glenable.md) com o argumento GL \_ automático \_ normal para gerar Normals de superfície de modo analítico, independentemente do conteúdo ou da habilitação do \_ mapa normal do GL map2 \_ .</span><span class="sxs-lookup"><span data-stu-id="c051c-124">If automatic normal generation is enabled, **glEvalCoord2fv** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="c051c-125">Permitir</span><span class="sxs-lookup"><span data-stu-id="c051c-125">Let</span></span>

![Equação mostrando um valor de produto cruzado para um mapa m.](images/evlcrd01.png)

<span data-ttu-id="c051c-127">O **n** normal gerado é</span><span class="sxs-lookup"><span data-stu-id="c051c-127">The generated normal **n** is</span></span>

![Equação mostrando o n normal gerado para o mapa.](images/evlcrd02.png)

<span data-ttu-id="c051c-129">As funções a seguir recuperam informações relacionadas à função **glEvalCoord2fv** :</span><span class="sxs-lookup"><span data-stu-id="c051c-129">The following functions retrieve information related to the **glEvalCoord2fv** function:</span></span>

<span data-ttu-id="c051c-130">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 3</span><span class="sxs-lookup"><span data-stu-id="c051c-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="c051c-131">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="c051c-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="c051c-132">índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_</span><span class="sxs-lookup"><span data-stu-id="c051c-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="c051c-133">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="c051c-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="c051c-134">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="c051c-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="c051c-135">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="c051c-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="c051c-136">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="c051c-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="c051c-137">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="c051c-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="c051c-138">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="c051c-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="c051c-139">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 3</span><span class="sxs-lookup"><span data-stu-id="c051c-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="c051c-140">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="c051c-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="c051c-141">índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_</span><span class="sxs-lookup"><span data-stu-id="c051c-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="c051c-142">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="c051c-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="c051c-143">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="c051c-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="c051c-144">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="c051c-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="c051c-145">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="c051c-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="c051c-146">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="c051c-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="c051c-147">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="c051c-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="c051c-148">[**glIsEnabled**](glisenabled.md) com Argument GL \_ automático \_ normal</span><span class="sxs-lookup"><span data-stu-id="c051c-148">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="c051c-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c051c-149">Requirements</span></span>



| <span data-ttu-id="c051c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="c051c-150">Requirement</span></span> | <span data-ttu-id="c051c-151">Valor</span><span class="sxs-lookup"><span data-stu-id="c051c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c051c-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c051c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c051c-153">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c051c-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c051c-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c051c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c051c-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c051c-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c051c-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c051c-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="c051c-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c051c-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c051c-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c051c-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="c051c-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c051c-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c051c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="c051c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c051c-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c051c-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c051c-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="c051c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c051c-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c051c-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c051c-164">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c051c-164">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c051c-165">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="c051c-165">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="c051c-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="c051c-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="c051c-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c051c-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c051c-168">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="c051c-168">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="c051c-169">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="c051c-169">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="c051c-170">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="c051c-170">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="c051c-171">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c051c-171">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c051c-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="c051c-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="c051c-173">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="c051c-173">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="c051c-174">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="c051c-174">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="c051c-175">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="c051c-175">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="c051c-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="c051c-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="c051c-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="c051c-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c051c-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="c051c-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





