---
title: função glTexEnvfv (GL. h)
description: A função glTexEnvfv define um parâmetro de ambiente de textura.
ms.assetid: 7b8e65aa-1b5c-47ab-8d6c-df14c90075a8
keywords:
- função glTexEnvfv OpenGL
topic_type:
- apiref
api_name:
- glTexEnvfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a2b74025deee08d2d895af0012e85e19ac269b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769205"
---
# <a name="gltexenvfv-function"></a><span data-ttu-id="a50de-104">função glTexEnvfv</span><span class="sxs-lookup"><span data-stu-id="a50de-104">glTexEnvfv function</span></span>

<span data-ttu-id="a50de-105">A função **glTexEnvfv** define um parâmetro de ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="a50de-105">The **glTexEnvfv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a50de-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a50de-106">Syntax</span></span>


```C++
void WINAPI glTexEnvfv(
         GLenum  target,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="a50de-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a50de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50de-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="a50de-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a50de-109">Um ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="a50de-109">A texture environment.</span></span> <span data-ttu-id="a50de-110">Deve ser GL \_ Texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="a50de-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="a50de-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="a50de-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="a50de-112">O nome simbólico de um parâmetro de ambiente de textura de valor único.</span><span class="sxs-lookup"><span data-stu-id="a50de-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="a50de-113">Os valores aceitos são o GL \_ Texture \_ env \_ Mode e GL \_ Texture \_ env \_ Color.</span><span class="sxs-lookup"><span data-stu-id="a50de-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="a50de-114">*params*</span><span class="sxs-lookup"><span data-stu-id="a50de-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a50de-115">Um ponteiro para uma matriz de parâmetros: uma única constante simbólica ou uma cor RGBA.</span><span class="sxs-lookup"><span data-stu-id="a50de-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50de-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a50de-116">Return value</span></span>

<span data-ttu-id="a50de-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a50de-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a50de-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a50de-118">Error codes</span></span>

<span data-ttu-id="a50de-119">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a50de-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a50de-120">Nome</span><span class="sxs-lookup"><span data-stu-id="a50de-120">Name</span></span>                                                                                                  | <span data-ttu-id="a50de-121">Significado</span><span class="sxs-lookup"><span data-stu-id="a50de-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a50de-122"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="a50de-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a50de-123">*target* ou *pname* não era um dos valores definidos aceitos, ou quando *params* deveria ter tido um valor constante definido (com base no valor de *pname*) e não.</span><span class="sxs-lookup"><span data-stu-id="a50de-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="a50de-124"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a50de-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a50de-125">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a50de-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="a50de-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a50de-126">Remarks</span></span>

<span data-ttu-id="a50de-127">Um ambiente de textura especifica como os valores de textura são interpretados quando um fragmento é texturizado.</span><span class="sxs-lookup"><span data-stu-id="a50de-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="a50de-128">O parâmetro de *destino* deve ser GL \_ Texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="a50de-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="a50de-129">O parâmetro *pname* pode ser GL \_ Texture env \_ \_ Mode ou GL \_ Texture \_ env \_ Color.</span><span class="sxs-lookup"><span data-stu-id="a50de-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="a50de-130">Se *pname* for \_ \_ \_ o modo de textura de env GL, *params* será (ou apontará) o nome simbólico de uma função de textura.</span><span class="sxs-lookup"><span data-stu-id="a50de-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="a50de-131">Três funções de textura são definidas: GL \_ modular, GL \_ Decal e GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="a50de-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="a50de-132">Uma função de textura age no fragmento para ser texturizada usando o valor da imagem de textura que se aplica ao fragmento (consulte [**glTexParameter**](gltexparameter-functions.md)) e produz uma cor RGBA para esse fragmento.</span><span class="sxs-lookup"><span data-stu-id="a50de-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="a50de-133">A tabela a seguir mostra como a cor RGBA é produzida para cada uma das três funções de textura que podem ser escolhidas.</span><span class="sxs-lookup"><span data-stu-id="a50de-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="a50de-134">*C* é um triplo de valores de cor (RGB) e *um* é o valor alfa associado.</span><span class="sxs-lookup"><span data-stu-id="a50de-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="a50de-135">Os valores RGBA extraídos de uma imagem de textura estão no intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="a50de-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="a50de-136">O *f* de subscrito refere-se ao fragmento de entrada, ao *t* de subscrito à imagem de textura, ao *c* de cor do ambiente de textura e a um subscrito *v* indica um valor produzido pela função de textura.</span><span class="sxs-lookup"><span data-stu-id="a50de-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="a50de-137">Uma imagem de textura pode ter até quatro componentes por elemento de textura (consulte [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="a50de-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="a50de-138">Em uma imagem de um componente, o lt indica que há um único componente.</span><span class="sxs-lookup"><span data-stu-id="a50de-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="a50de-139">Uma imagem de dois componentes usa *L?*</span><span class="sxs-lookup"><span data-stu-id="a50de-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="a50de-140">e *um?*</span><span class="sxs-lookup"><span data-stu-id="a50de-140">and *A?*</span></span> <span data-ttu-id="a50de-141">.</span><span class="sxs-lookup"><span data-stu-id="a50de-141">.</span></span> <span data-ttu-id="a50de-142">Uma imagem de três componentes tem apenas um valor de cor, *C?*</span><span class="sxs-lookup"><span data-stu-id="a50de-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="a50de-143">.</span><span class="sxs-lookup"><span data-stu-id="a50de-143">.</span></span> <span data-ttu-id="a50de-144">Uma imagem de quatro componentes tem um valor de cor *C?*</span><span class="sxs-lookup"><span data-stu-id="a50de-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="a50de-145">e um valor alfa *A?*</span><span class="sxs-lookup"><span data-stu-id="a50de-145">and an alpha value *A?*</span></span> <span data-ttu-id="a50de-146">.</span><span class="sxs-lookup"><span data-stu-id="a50de-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a50de-147">Número de componentes</span><span class="sxs-lookup"><span data-stu-id="a50de-147">Number of components</span></span></th>
<th><span data-ttu-id="a50de-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="a50de-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="a50de-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="a50de-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="a50de-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="a50de-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a50de-151">1 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="a50de-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a50de-152"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-152"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="a50de-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a50de-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="a50de-154">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a50de-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a50de-155"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-155"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="a50de-156"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="a50de-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="a50de-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a50de-158"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a50de-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a50de-159"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a50de-159"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a50de-160">2 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="a50de-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a50de-161"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-161"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="a50de-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a50de-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="a50de-163">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a50de-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a50de-164"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-164"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="a50de-165"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="a50de-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="a50de-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a50de-167"><em>A</em> <em><sub>v</sub></em>   =  <em>a<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a50de-167"><em>A</em> <em><sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a50de-168"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a50de-168"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a50de-169">3 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="a50de-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a50de-170"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-170"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="a50de-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a50de-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a50de-172"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-172"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="a50de-173">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a50de-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a50de-174"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="a50de-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="a50de-175"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a50de-175"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a50de-176">4 $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="a50de-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a50de-177"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-177"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="a50de-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a50de-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a50de-179"><em>C<sub>v</sub> </em> = (1- <em>a?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-179"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="a50de-180"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="a50de-181"><em>&?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="a50de-182">Não definido $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a50de-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a50de-183"><em>Um<sub>v</sub> </em>  =  <em>R?</em></span><span class="sxs-lookup"><span data-stu-id="a50de-183"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="a50de-184"><em>Um<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="a50de-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="a50de-185"><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a50de-185"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="a50de-186">Se pname for GL \_ Texture \_ env \_ Color, *params* é um ponteiro para uma matriz que contém uma cor RGBA que consiste em quatro valores.</span><span class="sxs-lookup"><span data-stu-id="a50de-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="a50de-187">Os componentes de cor de inteiro são interpretados linearmente de forma que o inteiro mais positivo seja mapeado para 1,0 e o número inteiro mais negativo seja mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="a50de-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="a50de-188">Os valores são clamped para o intervalo de \[ 0, 1 \] quando são especificados.</span><span class="sxs-lookup"><span data-stu-id="a50de-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="a50de-189">*C <sub>c</sub>* usa esses quatro valores.</span><span class="sxs-lookup"><span data-stu-id="a50de-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="a50de-190">O \_ modo de textura de env GL usa como padrão \_ \_ a \_ cor do GL modular e GL de \_ textura de \_ \_ cores env para (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="a50de-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="a50de-191">A função a seguir recupera informações relacionadas a **glTexEnvfv**:</span><span class="sxs-lookup"><span data-stu-id="a50de-191">The following function retrieves information related to **glTexEnvfv**:</span></span>

[<span data-ttu-id="a50de-192">**glTexGetEnvfv**</span><span class="sxs-lookup"><span data-stu-id="a50de-192">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="a50de-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a50de-193">Requirements</span></span>



| <span data-ttu-id="a50de-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="a50de-194">Requirement</span></span> | <span data-ttu-id="a50de-195">Valor</span><span class="sxs-lookup"><span data-stu-id="a50de-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a50de-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a50de-196">Minimum supported client</span></span><br/> | <span data-ttu-id="a50de-197">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a50de-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a50de-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a50de-198">Minimum supported server</span></span><br/> | <span data-ttu-id="a50de-199">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a50de-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a50de-200">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a50de-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="a50de-201"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a50de-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a50de-202">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a50de-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="a50de-203"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a50de-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a50de-204">DLL</span><span class="sxs-lookup"><span data-stu-id="a50de-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a50de-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a50de-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a50de-206">Confira também</span><span class="sxs-lookup"><span data-stu-id="a50de-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a50de-207">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a50de-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a50de-208">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a50de-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a50de-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a50de-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a50de-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a50de-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="a50de-211">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a50de-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





