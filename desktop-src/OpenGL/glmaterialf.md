---
title: função glMaterialf (GL. h)
description: A função glMaterialf especifica os parâmetros materiais para o modelo de iluminação.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- função glMaterialf OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c77cb1be5595f4a872988bbc6480d4cd6f65aae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760218"
---
# <a name="glmaterialf-function"></a><span data-ttu-id="a888a-104">função glMaterialf</span><span class="sxs-lookup"><span data-stu-id="a888a-104">glMaterialf function</span></span>

<span data-ttu-id="a888a-105">A função **glMaterialf** especifica os parâmetros materiais para o modelo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="a888a-105">The **glMaterialf** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="a888a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a888a-106">Syntax</span></span>


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="a888a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a888a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a888a-108">*sorridente*</span><span class="sxs-lookup"><span data-stu-id="a888a-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="a888a-109">A face ou faces que estão sendo atualizadas.</span><span class="sxs-lookup"><span data-stu-id="a888a-109">The face or faces that are being updated.</span></span> <span data-ttu-id="a888a-110">Deve ser um dos seguintes: GL \_ frontal, GL \_ voltar ou GL \_ front e GL de \_ volta.</span><span class="sxs-lookup"><span data-stu-id="a888a-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="a888a-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="a888a-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="a888a-112">O parâmetro de material de valor único da face ou faces sendo atualizadas.</span><span class="sxs-lookup"><span data-stu-id="a888a-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="a888a-113">Deve ter o GL de \_ luminosidade.</span><span class="sxs-lookup"><span data-stu-id="a888a-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="a888a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a888a-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="a888a-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a888a-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="a888a-116"><dt>**claridade do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a888a-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="a888a-117">O parâmetro *param* é um único valor de ponto flutuante que especifica o expoente de especular RGBA do material.</span><span class="sxs-lookup"><span data-stu-id="a888a-117">The *param* parameter is a single floating-point value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="a888a-118">Os valores inteiros são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="a888a-118">Integer values are mapped directly.</span></span> <span data-ttu-id="a888a-119">Somente os valores no intervalo de \[ 0, 128 \] são aceitos.</span><span class="sxs-lookup"><span data-stu-id="a888a-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="a888a-120">O expoente especular padrão para os materiais front-end e traseiro é 0.</span><span class="sxs-lookup"><span data-stu-id="a888a-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a888a-121">*param*</span><span class="sxs-lookup"><span data-stu-id="a888a-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="a888a-122">O valor para o qual o parâmetro GL \_ luminosidade será definido.</span><span class="sxs-lookup"><span data-stu-id="a888a-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a888a-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a888a-123">Return value</span></span>

<span data-ttu-id="a888a-124">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a888a-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a888a-125">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a888a-125">Error codes</span></span>

<span data-ttu-id="a888a-126">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a888a-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a888a-127">Nome</span><span class="sxs-lookup"><span data-stu-id="a888a-127">Name</span></span>                                                                                              | <span data-ttu-id="a888a-128">Significado</span><span class="sxs-lookup"><span data-stu-id="a888a-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a888a-129"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="a888a-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="a888a-130">A *face* ou a *pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="a888a-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="a888a-131"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a888a-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="a888a-132">Um expoente especular fora do intervalo de \[ 0, 128 \] foi especificado.</span><span class="sxs-lookup"><span data-stu-id="a888a-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a888a-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="a888a-133">Remarks</span></span>

<span data-ttu-id="a888a-134">A função **glMaterialf** atribui valores a parâmetros materiais.</span><span class="sxs-lookup"><span data-stu-id="a888a-134">The **glMaterialf** function assigns values to material parameters.</span></span> <span data-ttu-id="a888a-135">Há dois conjuntos correspondentes de parâmetros materiais.</span><span class="sxs-lookup"><span data-stu-id="a888a-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="a888a-136">Um, o conjunto *front-end* , é usado para sombrear pontos, linhas, bitmaps e todos os polígonos (quando a iluminação de dois lados está desabilitada) ou apenas polígonos frontais (quando a iluminação de dois lados está habilitada).</span><span class="sxs-lookup"><span data-stu-id="a888a-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="a888a-137">O outro conjunto, *voltado*, é usado para sombrear polígonos voltados somente quando a iluminação de dois lados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="a888a-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="a888a-138">Consulte [**glLightModel**](gllightmodel-functions.md) para obter detalhes sobre cálculos de iluminação de um lado e dois lados.</span><span class="sxs-lookup"><span data-stu-id="a888a-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="a888a-139">A função **glMaterialf** usa três argumentos.</span><span class="sxs-lookup"><span data-stu-id="a888a-139">The **glMaterialf** function takes three arguments.</span></span> <span data-ttu-id="a888a-140">A primeira, *face*, especifica se o \_ material frontal do GL, os \_ materiais traseiros do GL ou os \_ materiais de frente \_ e de trás do GL \_ serão modificados.</span><span class="sxs-lookup"><span data-stu-id="a888a-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="a888a-141">O segundo, *pname*, especifica qual dos vários parâmetros em um ou ambos os conjuntos serão modificados.</span><span class="sxs-lookup"><span data-stu-id="a888a-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="a888a-142">O terceiro, *param*, especifica qual valor será atribuído ao parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="a888a-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="a888a-143">Os parâmetros materiais são usados na equação de iluminação que é opcionalmente aplicada a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="a888a-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="a888a-144">A equação é discutida em [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a888a-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="a888a-145">Os parâmetros de material podem ser atualizados a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a888a-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="a888a-146">Em particular, **glMaterialf** pode ser chamado entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a888a-146">In particular, **glMaterialf** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="a888a-147">Se apenas um parâmetro de material único for alterado por vértice, no entanto, [**glColorMaterial**](glcolormaterial.md) será preferencial em relação a **glMaterialf**.</span><span class="sxs-lookup"><span data-stu-id="a888a-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialf**.</span></span>

<span data-ttu-id="a888a-148">A função a seguir recupera informações relacionadas a **glMaterialf**:</span><span class="sxs-lookup"><span data-stu-id="a888a-148">The following function retrieves information related to **glMaterialf**:</span></span>

[<span data-ttu-id="a888a-149">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="a888a-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="a888a-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a888a-150">Requirements</span></span>



| <span data-ttu-id="a888a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="a888a-151">Requirement</span></span> | <span data-ttu-id="a888a-152">Valor</span><span class="sxs-lookup"><span data-stu-id="a888a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a888a-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a888a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a888a-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a888a-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a888a-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a888a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a888a-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a888a-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a888a-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a888a-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a888a-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a888a-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a888a-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a888a-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="a888a-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a888a-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a888a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="a888a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a888a-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a888a-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a888a-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="a888a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a888a-164">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="a888a-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="a888a-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="a888a-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="a888a-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="a888a-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





