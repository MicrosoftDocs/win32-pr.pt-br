---
title: função glTexEnvf (GL. h)
description: A função glTexEnvf define um parâmetro de ambiente de textura.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- função glTexEnvf OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644556"
---
# <a name="gltexenvf-function"></a><span data-ttu-id="1031d-104">função glTexEnvf</span><span class="sxs-lookup"><span data-stu-id="1031d-104">glTexEnvf function</span></span>

<span data-ttu-id="1031d-105">A função **glTexEnvf** define um parâmetro de ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="1031d-105">The **glTexEnvf** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1031d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1031d-106">Syntax</span></span>


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="1031d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1031d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1031d-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="1031d-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="1031d-109">Um ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="1031d-109">A texture environment.</span></span> <span data-ttu-id="1031d-110">Deve ser GL \_ Texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="1031d-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="1031d-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="1031d-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="1031d-112">O nome simbólico de um parâmetro de ambiente de textura de valor único.</span><span class="sxs-lookup"><span data-stu-id="1031d-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="1031d-113">Deve ser GL \_ \_ Mode Texture env \_ .</span><span class="sxs-lookup"><span data-stu-id="1031d-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="1031d-114">*param*</span><span class="sxs-lookup"><span data-stu-id="1031d-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="1031d-115">Uma única constante simbólica, uma do GL \_ modular \_ Decal, GL \_ Blend ou GL \_ replace.</span><span class="sxs-lookup"><span data-stu-id="1031d-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1031d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1031d-116">Return value</span></span>

<span data-ttu-id="1031d-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1031d-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1031d-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1031d-118">Error codes</span></span>

<span data-ttu-id="1031d-119">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1031d-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1031d-120">Name</span><span class="sxs-lookup"><span data-stu-id="1031d-120">Name</span></span>                                                                                                  | <span data-ttu-id="1031d-121">Significado</span><span class="sxs-lookup"><span data-stu-id="1031d-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1031d-122"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1031d-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1031d-123">*target* ou *pname* não era um dos valores definidos aceitos, ou quando *params* deveria ter tido um valor constante definido (com base no valor de *pname*) e não.</span><span class="sxs-lookup"><span data-stu-id="1031d-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="1031d-124"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1031d-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1031d-125">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1031d-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="1031d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1031d-126">Remarks</span></span>

<span data-ttu-id="1031d-127">Um ambiente de textura especifica como os valores de textura são interpretados quando um fragmento é texturizado.</span><span class="sxs-lookup"><span data-stu-id="1031d-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="1031d-128">O parâmetro de *destino* deve ser GL \_ Texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="1031d-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="1031d-129">O parâmetro *pname* é GL \_ Texture \_ env \_ Mode.</span><span class="sxs-lookup"><span data-stu-id="1031d-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="1031d-130">Três funções de textura são definidas: GL \_ modular, GL \_ Decal e GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="1031d-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="1031d-131">Uma função de textura age no fragmento para ser texturizada usando o valor da imagem de textura que se aplica ao fragmento (consulte [**glTexParameter**](gltexparameter-functions.md)) e produz uma cor RGBA para esse fragmento.</span><span class="sxs-lookup"><span data-stu-id="1031d-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="1031d-132">A tabela a seguir mostra como a cor RGBA é produzida para cada uma das três funções de textura que podem ser escolhidas.</span><span class="sxs-lookup"><span data-stu-id="1031d-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="1031d-133">*C* é um triplo de valores de cor (RGB) e *um* é o valor alfa associado.</span><span class="sxs-lookup"><span data-stu-id="1031d-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="1031d-134">Os valores RGBA extraídos de uma imagem de textura estão no intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="1031d-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="1031d-135">O *f* de subscrito refere-se ao fragmento de entrada, ao *t* de subscrito à imagem de textura, ao *c* de cor do ambiente de textura e a um subscrito *v* indica um valor produzido pela função de textura.</span><span class="sxs-lookup"><span data-stu-id="1031d-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="1031d-136">Uma imagem de textura pode ter até quatro componentes por elemento de textura (consulte [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="1031d-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="1031d-137">Em uma imagem de um componente, o lt indica que há um único componente.</span><span class="sxs-lookup"><span data-stu-id="1031d-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="1031d-138">Uma imagem de dois componentes usa *L?*</span><span class="sxs-lookup"><span data-stu-id="1031d-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="1031d-139">e *um?*</span><span class="sxs-lookup"><span data-stu-id="1031d-139">and *A?*</span></span> <span data-ttu-id="1031d-140">.</span><span class="sxs-lookup"><span data-stu-id="1031d-140">.</span></span> <span data-ttu-id="1031d-141">Uma imagem de três componentes tem apenas um valor de cor, *C?*</span><span class="sxs-lookup"><span data-stu-id="1031d-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="1031d-142">.</span><span class="sxs-lookup"><span data-stu-id="1031d-142">.</span></span> <span data-ttu-id="1031d-143">Uma imagem de quatro componentes tem um valor de cor *C?*</span><span class="sxs-lookup"><span data-stu-id="1031d-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="1031d-144">e um valor alfa *A?*</span><span class="sxs-lookup"><span data-stu-id="1031d-144">and an alpha value *A?*</span></span> <span data-ttu-id="1031d-145">.</span><span class="sxs-lookup"><span data-stu-id="1031d-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1031d-146">Número de componentes</span><span class="sxs-lookup"><span data-stu-id="1031d-146">Number of components</span></span></th>
<th><span data-ttu-id="1031d-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="1031d-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="1031d-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="1031d-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="1031d-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="1031d-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="1031d-150">1 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="1031d-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1031d-151"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="1031d-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="1031d-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="1031d-153">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1031d-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1031d-154"><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-154"><em>C</em> <em><sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="1031d-155"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="1031d-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="1031d-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1031d-157"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="1031d-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="1031d-158"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="1031d-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="1031d-159">2 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="1031d-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1031d-160"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="1031d-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="1031d-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="1031d-162">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1031d-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1031d-163"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="1031d-164"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="1031d-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="1031d-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1031d-166"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="1031d-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="1031d-167"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="1031d-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="1031d-168">3 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="1031d-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1031d-169"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="1031d-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="1031d-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="1031d-171"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="1031d-172">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1031d-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1031d-173"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="1031d-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="1031d-174"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="1031d-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="1031d-175">4 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="1031d-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1031d-176"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="1031d-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="1031d-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="1031d-178"><em>C<sub>v</sub> </em> = (1- <em>a?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="1031d-179"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="1031d-180"><em>&?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="1031d-181">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1031d-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1031d-182"><em>Um<sub>v</sub> </em>  =  <em>R?</em></span><span class="sxs-lookup"><span data-stu-id="1031d-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="1031d-183"><em>Um<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="1031d-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="1031d-184"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="1031d-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="1031d-185">O \_ modo de textura de \_ env GL \_ usa como padrão o GL \_ modular.</span><span class="sxs-lookup"><span data-stu-id="1031d-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="1031d-186">A função a seguir recupera informações relacionadas a **glTexEnvf**:</span><span class="sxs-lookup"><span data-stu-id="1031d-186">The following function retrieves information related to **glTexEnvf**:</span></span>

[<span data-ttu-id="1031d-187">**glTexGetEnvfv**</span><span class="sxs-lookup"><span data-stu-id="1031d-187">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="1031d-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1031d-188">Requirements</span></span>



| <span data-ttu-id="1031d-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="1031d-189">Requirement</span></span> | <span data-ttu-id="1031d-190">Valor</span><span class="sxs-lookup"><span data-stu-id="1031d-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1031d-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1031d-191">Minimum supported client</span></span><br/> | <span data-ttu-id="1031d-192">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1031d-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1031d-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1031d-193">Minimum supported server</span></span><br/> | <span data-ttu-id="1031d-194">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1031d-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1031d-195">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1031d-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="1031d-196"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1031d-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1031d-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1031d-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="1031d-198"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1031d-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1031d-199">DLL</span><span class="sxs-lookup"><span data-stu-id="1031d-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1031d-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1031d-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1031d-201">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1031d-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1031d-202">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1031d-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1031d-203">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1031d-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1031d-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1031d-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1031d-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1031d-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1031d-206">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1031d-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





