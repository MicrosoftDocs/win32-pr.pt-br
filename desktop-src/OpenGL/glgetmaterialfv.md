---
title: função glGetMaterialfv (GL. h)
description: As funções glGetMaterialfv e glGetMaterialiv retornam os parâmetros materiais. | função glGetMaterialfv (GL. h)
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- função glGetMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce33ee1f88d492f67cf3ebb93c575f8f36d1ffa0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298155"
---
# <a name="glgetmaterialfv-function"></a><span data-ttu-id="93569-105">função glGetMaterialfv</span><span class="sxs-lookup"><span data-stu-id="93569-105">glGetMaterialfv function</span></span>

<span data-ttu-id="93569-106">As funções **glGetMaterialfv** e [**glGetMaterialiv**](glgetmaterialiv.md) retornam os parâmetros materiais.</span><span class="sxs-lookup"><span data-stu-id="93569-106">The **glGetMaterialfv** and [**glGetMaterialiv**](glgetmaterialiv.md) functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="93569-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93569-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialfv(
   GLenum  face,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="93569-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93569-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93569-109">*sorridente*</span><span class="sxs-lookup"><span data-stu-id="93569-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="93569-110">Especifica qual dos dois materiais está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="93569-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="93569-111">\_O GL frontal ou GL \_ traseiro são aceitos, representando os materiais de frente e de trás, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="93569-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="93569-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="93569-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="93569-113">O parâmetro material a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="93569-113">The material parameter to return.</span></span> <span data-ttu-id="93569-114">Os valores a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="93569-114">The following values are accepted.</span></span>



| <span data-ttu-id="93569-115">Valor</span><span class="sxs-lookup"><span data-stu-id="93569-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="93569-116">Significado</span><span class="sxs-lookup"><span data-stu-id="93569-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="93569-117"><dt>**\_ambiente GL**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="93569-118">O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a representação de ambiente do material.</span><span class="sxs-lookup"><span data-stu-id="93569-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="93569-119">Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o valor inteiro representável mais positivo e-1,0 é mapeado para o valor inteiro reapresentável mais negativo.</span><span class="sxs-lookup"><span data-stu-id="93569-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="93569-120">Se o valor interno estiver fora do intervalo \[ -1, 1 \] , o valor de retorno de inteiro correspondente será indefinido.</span><span class="sxs-lookup"><span data-stu-id="93569-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="93569-121"><dt>**\_difusão GL**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="93569-122">O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a reflexão difusa do material.</span><span class="sxs-lookup"><span data-stu-id="93569-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="93569-123">Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o valor inteiro representável mais positivo e-1,0 é mapeado para o valor inteiro reapresentável mais negativo.</span><span class="sxs-lookup"><span data-stu-id="93569-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="93569-124">Se o valor interno estiver fora do intervalo \[ -1, 1 \] , o valor de retorno de inteiro correspondente será indefinido.</span><span class="sxs-lookup"><span data-stu-id="93569-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="93569-125"><dt>**\_ESPECULA GL**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="93569-126">O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a representação especular do material.</span><span class="sxs-lookup"><span data-stu-id="93569-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="93569-127">Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o valor inteiro representável mais positivo e-1,0 é mapeado para o valor inteiro reapresentável mais negativo.</span><span class="sxs-lookup"><span data-stu-id="93569-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="93569-128">Se o valor interno estiver fora do intervalo \[ -1, 1 \] , o valor de retorno de inteiro correspondente será indefinido.</span><span class="sxs-lookup"><span data-stu-id="93569-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="93569-129"><dt>**\_emissão GL**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="93569-130">O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade de luz emitida do material.</span><span class="sxs-lookup"><span data-stu-id="93569-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="93569-131">Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o valor inteiro representável mais positivo e-1,0 é mapeado para o valor inteiro reapresentável mais negativo.</span><span class="sxs-lookup"><span data-stu-id="93569-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="93569-132">Se o valor interno estiver fora do intervalo \[ -1, 1 \] , o valor de retorno de inteiro correspondente será indefinido.</span><span class="sxs-lookup"><span data-stu-id="93569-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="93569-133"><dt>**claridade do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="93569-134">O parâmetro *params* retorna um inteiro ou um valor de ponto flutuante que representa o expoente especular do material.</span><span class="sxs-lookup"><span data-stu-id="93569-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="93569-135">Os valores inteiros, quando solicitados, são calculados arredondando o valor de ponto flutuante interno para o valor inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="93569-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="93569-136"><dt>**\_índices de cores GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="93569-137">O parâmetro *params* retorna três valores inteiros ou de ponto flutuante que representam os índices ambiente, difuso e especular do material.</span><span class="sxs-lookup"><span data-stu-id="93569-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="93569-138">Use esses índices somente para a iluminação de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="93569-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="93569-139">(Os outros parâmetros são todos usados apenas para iluminação RGBA.) Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.</span><span class="sxs-lookup"><span data-stu-id="93569-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="93569-140">*params*</span><span class="sxs-lookup"><span data-stu-id="93569-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="93569-141">Retorna os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="93569-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93569-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93569-142">Return value</span></span>

<span data-ttu-id="93569-143">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="93569-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="93569-144">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="93569-144">Error codes</span></span>

<span data-ttu-id="93569-145">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="93569-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="93569-146">Nome</span><span class="sxs-lookup"><span data-stu-id="93569-146">Name</span></span>                                                                                                  | <span data-ttu-id="93569-147">Significado</span><span class="sxs-lookup"><span data-stu-id="93569-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93569-148"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="93569-149">o *destino* ou a *consulta* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="93569-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="93569-150"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="93569-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="93569-151">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="93569-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="93569-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="93569-152">Remarks</span></span>

<span data-ttu-id="93569-153">A função **glGetMaterial** retorna em *params* o valor ou os valores do parâmetro *pname* do material *face*.</span><span class="sxs-lookup"><span data-stu-id="93569-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="93569-154">Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.</span><span class="sxs-lookup"><span data-stu-id="93569-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="93569-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93569-155">Requirements</span></span>



| <span data-ttu-id="93569-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="93569-156">Requirement</span></span> | <span data-ttu-id="93569-157">Valor</span><span class="sxs-lookup"><span data-stu-id="93569-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93569-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93569-158">Minimum supported client</span></span><br/> | <span data-ttu-id="93569-159">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93569-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="93569-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93569-160">Minimum supported server</span></span><br/> | <span data-ttu-id="93569-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93569-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93569-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="93569-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="93569-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="93569-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="93569-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93569-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="93569-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93569-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="93569-166">DLL</span><span class="sxs-lookup"><span data-stu-id="93569-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93569-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93569-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93569-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="93569-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93569-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="93569-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="93569-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="93569-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="93569-171">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="93569-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





