---
description: Renderiza uma textura em um arquivo e retorna o resultado para o host asynchrnously.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: RenderTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500418"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span data-ttu-id="dcc4c-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: RenderTextureAsync</span><span class="sxs-lookup"><span data-stu-id="dcc4c-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync method</span></span>

<span data-ttu-id="dcc4c-104">Renderiza uma textura em um arquivo e retorna o resultado para o host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-104">Renders a texture to a file and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc4c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcc4c-105">Syntax</span></span>


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="dcc4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcc4c-106">Parameters</span></span>

<span data-ttu-id="dcc4c-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-107">*textureId* </span></span>  
<span data-ttu-id="dcc4c-108">A ID da textura a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-108">The ID of the texture to render.</span></span>

<span data-ttu-id="dcc4c-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-109">*sliceIndex* </span></span>  
<span data-ttu-id="dcc4c-110">O índice da fatia dentro da textura a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-110">The index of the slice within the texture to render.</span></span>

<span data-ttu-id="dcc4c-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-111">*formatOverride* </span></span>  
<span data-ttu-id="dcc4c-112">A substituição do formato de cor.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-112">The color format override.</span></span>

<span data-ttu-id="dcc4c-113">*canto*</span><span class="sxs-lookup"><span data-stu-id="dcc4c-113">*lower*</span></span>   

<span data-ttu-id="dcc4c-114">*canto superior*</span><span class="sxs-lookup"><span data-stu-id="dcc4c-114">*upper*</span></span>   

<span data-ttu-id="dcc4c-115">*shaderFileName* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-115">*shaderFileName* </span></span>  
<span data-ttu-id="dcc4c-116">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-116">A COM string containing the pathname of the shader file.</span></span>

<span data-ttu-id="dcc4c-117">*numFloatShaderVars* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-117">*numFloatShaderVars* </span></span>  
<span data-ttu-id="dcc4c-118">O número de variáveis do sombreador de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="dcc4c-118">The number of floating-point shader variables</span></span>

<span data-ttu-id="dcc4c-119">*count6 \_ shaderFloatVarName* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-119">*count6\_shaderFloatVarName* </span></span>  
<span data-ttu-id="dcc4c-120">Cadeias de caracteres COM contianing os nomes das variáveis do sombreador de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-120">COM strings contianing the names of the floating-point shader variables.</span></span>

<span data-ttu-id="dcc4c-121">*count6 \_ shaderFloatVarValue* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-121">*count6\_shaderFloatVarValue* </span></span>  
<span data-ttu-id="dcc4c-122">As variáveis do sombreador de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-122">The floating-point shader variables.</span></span>

<span data-ttu-id="dcc4c-123">*numBoolShaderVars* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-123">*numBoolShaderVars* </span></span>  
<span data-ttu-id="dcc4c-124">O número de variáveis de sombreador booliano.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-124">The number of boolean shader variables.</span></span>

<span data-ttu-id="dcc4c-125">*count9 \_ shaderBoolVarName* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-125">*count9\_shaderBoolVarName* </span></span>  
<span data-ttu-id="dcc4c-126">Cadeias de caracteres COM contianing os nomes das variáveis de sombreador booliano.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-126">COM strings contianing the names of the boolean shader variables.</span></span>

<span data-ttu-id="dcc4c-127">*count9 \_ shaderBoolVarValue* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-127">*count9\_shaderBoolVarValue* </span></span>  
<span data-ttu-id="dcc4c-128">As variáveis do sombreador booliano.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-128">The boolean shader variables.</span></span>

<span data-ttu-id="dcc4c-129">*renderContentFileName* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-129">*renderContentFileName* </span></span>  
<span data-ttu-id="dcc4c-130">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde a textura renderizada foi gravada.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-130">A COM string containing the pathname of the file where the rendered texture was written.</span></span>

<span data-ttu-id="dcc4c-131">*retornos* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-131">*callbacks* </span></span>  
<span data-ttu-id="dcc4c-132">O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-132">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="dcc4c-133">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-133">*requestCookie* </span></span>  
<span data-ttu-id="dcc4c-134">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-134">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="dcc4c-135">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="dcc4c-135">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="dcc4c-136">Não usado.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-136">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcc4c-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dcc4c-137">Return value</span></span>

<span data-ttu-id="dcc4c-138">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dcc4c-139">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dcc4c-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc4c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcc4c-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dcc4c-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dcc4c-141">Header</span></span></p></td><td><span data-ttu-id="dcc4c-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="dcc4c-142">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="dcc4c-143"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="dcc4c-143"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="dcc4c-144">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="dcc4c-144">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
