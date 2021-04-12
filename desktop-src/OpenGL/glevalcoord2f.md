---
title: função glEvalCoord2f (GL. h)
description: A função glEvalCoord2f avalia os mapas bidimensionais habilitados.
ms.assetid: feb2a324-9148-4e3f-8e6e-c545e36962c6
keywords:
- função glEvalCoord2f OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e586991b319e047957ae53362534c1bb0c90590
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104297831"
---
# <a name="glevalcoord2f-function"></a><span data-ttu-id="cc89b-104">função glEvalCoord2f</span><span class="sxs-lookup"><span data-stu-id="cc89b-104">glEvalCoord2f function</span></span>

<span data-ttu-id="cc89b-105">A função [**glEvalCoord2f**](glevalcoord2d.md) avalia os mapas bidimensionais habilitados.</span><span class="sxs-lookup"><span data-stu-id="cc89b-105">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc89b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc89b-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2f(
   GLfloat u,
   GLfloat v
);
```



## <a name="parameters"></a><span data-ttu-id="cc89b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc89b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc89b-108">*u*</span><span class="sxs-lookup"><span data-stu-id="cc89b-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="cc89b-109">Um valor que é o domínio coordena *u* para a função base definida em uma função [**glMap2**](glmap2.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="cc89b-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cc89b-110">*l*</span><span class="sxs-lookup"><span data-stu-id="cc89b-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="cc89b-111">Um valor que é o domínio coordena *v* para a função base definida em uma função [**glMap2**](glmap2.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="cc89b-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc89b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc89b-112">Return value</span></span>

<span data-ttu-id="cc89b-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cc89b-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc89b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc89b-114">Remarks</span></span>

<span data-ttu-id="cc89b-115">A função [**glEvalCoord2f**](glevalcoord2d.md) avalia os mapas bidimensionais habilitados usando dois valores de domínio, *u* e *v*.</span><span class="sxs-lookup"><span data-stu-id="cc89b-115">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="cc89b-116">Defina mapas com [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="cc89b-116">Define maps with [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="cc89b-117">Habilite ou desabilite-os com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="cc89b-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="cc89b-118">Quando uma das funções **glEvalCoord** é emitida, todos os mapas atualmente habilitados da dimensão indicada são avaliados.</span><span class="sxs-lookup"><span data-stu-id="cc89b-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="cc89b-119">Em seguida, para cada mapa habilitado, é como se a função OpenGL correspondente fosse emitida com o valor calculado.</span><span class="sxs-lookup"><span data-stu-id="cc89b-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="cc89b-120">Ou seja, se \_ \_ o índice GL MAP1 index ou GL \_ map2 \_ estiver habilitado, uma função [**glIndex**](glindex-functions.md) será simulada.</span><span class="sxs-lookup"><span data-stu-id="cc89b-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="cc89b-121">Se GL \_ MAP1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 estiver habilitado, uma função **glColor** será simulada.</span><span class="sxs-lookup"><span data-stu-id="cc89b-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="cc89b-122">Se GL \_ MAP1 \_ normal ou GL \_ map2 \_ normal estiver habilitado, um vetor normal é produzido e, se qualquer uma das \_ MAP1 de \_ textura GL \_ coord \_ 1, GL \_ MAP1 \_ Texture \_ coord \_ 2, GL \_ MAP1 de textura coord \_ \_ \_ 3, GL \_ MAP1 de \_ textura \_ coord \_ 4, GL map2 de textura coord \_ \_ \_ \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL map2 de textura \_ \_ \_ coord \_ 3 e GL \_ map2 Texture coord \_ \_ \_ 4 estiver habilitado, uma função [**glTexCoord**](gltexcoord-functions.md) apropriada será simulada.</span><span class="sxs-lookup"><span data-stu-id="cc89b-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="cc89b-123">O OpenGL usa valores avaliados em vez de valores atuais para as avaliações habilitadas e valores atuais de outra forma, para as coordenadas de cor, índice de cor, normal e textura.</span><span class="sxs-lookup"><span data-stu-id="cc89b-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="cc89b-124">No entanto, os valores avaliados não atualizam os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="cc89b-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="cc89b-125">Portanto, se as funções [**glVertex**](glvertex-functions.md) estiverem intercaladas com as funções **glEvalCoord** , as coordenadas Color, normal e Texture associadas às funções **glVertex** não serão afetadas pelos valores gerados pelas funções **glEvalCoord** , mas somente pelas funções [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) mais recentes.</span><span class="sxs-lookup"><span data-stu-id="cc89b-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="cc89b-126">Se a geração normal automática estiver habilitada, [**glEvalCoord2f**](glevalcoord2d.md) chamará [**glEnable**](glenable.md) com o argumento GL \_ automático \_ normal para gerar Normals de superfície de modo analítico, independentemente do conteúdo ou da habilitação do \_ mapa normal do GL map2 \_ .</span><span class="sxs-lookup"><span data-stu-id="cc89b-126">If automatic normal generation is enabled, [**glEvalCoord2f**](glevalcoord2d.md) calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="cc89b-127">Permitir</span><span class="sxs-lookup"><span data-stu-id="cc89b-127">Let</span></span>

![Equação mostrando um valor de produto cruzado para um mapa m.](images/evlcrd01.png)

<span data-ttu-id="cc89b-129">O **n** normal gerado é</span><span class="sxs-lookup"><span data-stu-id="cc89b-129">The generated normal **n** is</span></span>

![Equação mostrando o n normal gerado para o mapa.](images/evlcrd02.png)

<span data-ttu-id="cc89b-131">As funções a seguir recuperam informações relacionadas à função [**glEvalCoord2f**](glevalcoord2d.md) :</span><span class="sxs-lookup"><span data-stu-id="cc89b-131">The following functions retrieve information related to the [**glEvalCoord2f**](glevalcoord2d.md) function:</span></span>

<span data-ttu-id="cc89b-132">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 3</span><span class="sxs-lookup"><span data-stu-id="cc89b-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="cc89b-133">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc89b-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="cc89b-134">índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_</span><span class="sxs-lookup"><span data-stu-id="cc89b-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="cc89b-135">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc89b-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="cc89b-136">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="cc89b-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="cc89b-137">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="cc89b-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="cc89b-138">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="cc89b-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="cc89b-139">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="cc89b-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="cc89b-140">[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc89b-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="cc89b-141">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 3</span><span class="sxs-lookup"><span data-stu-id="cc89b-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="cc89b-142">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc89b-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="cc89b-143">índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_</span><span class="sxs-lookup"><span data-stu-id="cc89b-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="cc89b-144">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc89b-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="cc89b-145">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="cc89b-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="cc89b-146">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="cc89b-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="cc89b-147">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="cc89b-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="cc89b-148">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="cc89b-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="cc89b-149">[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc89b-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="cc89b-150">[**glIsEnabled**](glisenabled.md) com Argument GL \_ automático \_ normal</span><span class="sxs-lookup"><span data-stu-id="cc89b-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="cc89b-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc89b-151">Requirements</span></span>



| <span data-ttu-id="cc89b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc89b-152">Requirement</span></span> | <span data-ttu-id="cc89b-153">Valor</span><span class="sxs-lookup"><span data-stu-id="cc89b-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc89b-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc89b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="cc89b-155">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc89b-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cc89b-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc89b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="cc89b-157">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc89b-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc89b-158">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cc89b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc89b-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc89b-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cc89b-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc89b-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc89b-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc89b-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc89b-162">DLL</span><span class="sxs-lookup"><span data-stu-id="cc89b-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc89b-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc89b-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc89b-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc89b-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc89b-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cc89b-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cc89b-166">**glColor**</span><span class="sxs-lookup"><span data-stu-id="cc89b-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="cc89b-167">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="cc89b-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="cc89b-168">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="cc89b-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="cc89b-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cc89b-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cc89b-170">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="cc89b-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="cc89b-171">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="cc89b-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="cc89b-172">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="cc89b-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="cc89b-173">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="cc89b-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="cc89b-174">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="cc89b-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="cc89b-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="cc89b-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="cc89b-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="cc89b-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="cc89b-177">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="cc89b-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="cc89b-178">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="cc89b-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="cc89b-179">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="cc89b-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="cc89b-180">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="cc89b-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





