---
description: Crie um efeito de um arquivo.
ms.assetid: 1418857e-bda1-4ffb-bbb9-dfa3709313b1
title: Função D3DX10CreateEffectFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 60bc52e5b149a2fa69cc4a16f12900b12ab81db8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793821"
---
# <a name="d3dx10createeffectfromfile-function"></a><span data-ttu-id="63ea7-103">Função D3DX10CreateEffectFromFile</span><span class="sxs-lookup"><span data-stu-id="63ea7-103">D3DX10CreateEffectFromFile function</span></span>

<span data-ttu-id="63ea7-104">Crie um efeito de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="63ea7-104">Create an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ea7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63ea7-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="63ea7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63ea7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63ea7-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63ea7-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63ea7-109">Nome do arquivo de efeito ASCII.</span><span class="sxs-lookup"><span data-stu-id="63ea7-109">Name of the ASCII effect file.</span></span> <span data-ttu-id="63ea7-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="63ea7-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="63ea7-111">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="63ea7-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-112">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-113">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="63ea7-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="63ea7-114">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="63ea7-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-115">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-116">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="63ea7-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="63ea7-117">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="63ea7-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="63ea7-118">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="63ea7-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-119">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63ea7-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63ea7-121">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="63ea7-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-122">*HLSLFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63ea7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63ea7-124">HLSL opções de compilação (consulte as [ \_ constantes do sombreador d3d10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="63ea7-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-125">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63ea7-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63ea7-127">Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="63ea7-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-128">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-129">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="63ea7-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="63ea7-130">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="63ea7-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-131">*pEffectPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-131">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-132">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="63ea7-132">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="63ea7-133">Ponteiro para um pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartilhar variáveis entre efeitos.</span><span class="sxs-lookup"><span data-stu-id="63ea7-133">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-134">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-134">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-135">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="63ea7-135">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="63ea7-136">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="63ea7-136">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="63ea7-137">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="63ea7-137">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-138">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-138">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-139">Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="63ea7-139">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="63ea7-140">Endereço de um ponteiro para o efeito (consulte a [**interface ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) que é criada.</span><span class="sxs-lookup"><span data-stu-id="63ea7-140">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-141">*ppErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-141">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-142">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="63ea7-142">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="63ea7-143">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="63ea7-143">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="63ea7-144">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63ea7-144">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63ea7-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="63ea7-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="63ea7-146">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="63ea7-146">A pointer to the return value.</span></span> <span data-ttu-id="63ea7-147">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="63ea7-147">May be **NULL**.</span></span> <span data-ttu-id="63ea7-148">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="63ea7-148">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63ea7-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63ea7-149">Return value</span></span>

<span data-ttu-id="63ea7-150">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63ea7-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63ea7-151">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="63ea7-151">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63ea7-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63ea7-152">Requirements</span></span>



| <span data-ttu-id="63ea7-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ea7-153">Requirement</span></span> | <span data-ttu-id="63ea7-154">Valor</span><span class="sxs-lookup"><span data-stu-id="63ea7-154">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ea7-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63ea7-155">Header</span></span><br/> | <dl> <span data-ttu-id="63ea7-156"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="63ea7-156"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ea7-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="63ea7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ea7-158">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="63ea7-158">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
