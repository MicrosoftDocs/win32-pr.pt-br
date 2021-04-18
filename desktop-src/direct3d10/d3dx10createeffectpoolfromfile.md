---
description: Crie um pool de efeitos a partir de um arquivo de efeito.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: Função D3DX10CreateEffectPoolFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 418ea287b9bbf2021f3b2e5379b209cf87745a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793745"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a><span data-ttu-id="84841-103">Função D3DX10CreateEffectPoolFromFile</span><span class="sxs-lookup"><span data-stu-id="84841-103">D3DX10CreateEffectPoolFromFile function</span></span>

<span data-ttu-id="84841-104">Crie um pool de efeitos a partir de um arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="84841-104">Create an effect pool from an effect file.</span></span>

## <a name="syntax"></a><span data-ttu-id="84841-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84841-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="84841-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84841-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84841-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84841-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84841-109">O nome do arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="84841-109">The effect filename.</span></span> <span data-ttu-id="84841-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="84841-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="84841-111">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="84841-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="84841-112">*pDefines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-113">Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="84841-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="84841-114">Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.</span><span class="sxs-lookup"><span data-stu-id="84841-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="84841-115">*pInclude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-116">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="84841-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="84841-117">Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="84841-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="84841-118">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="84841-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="84841-119">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84841-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84841-121">Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="84841-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="84841-122">*HLSLFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84841-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84841-124">HLSL opções de compilação (consulte as [ \_ constantes do sombreador d3d10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="84841-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="84841-125">*FXFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84841-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84841-127">Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="84841-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="84841-128">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-129">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="84841-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="84841-130">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.</span><span class="sxs-lookup"><span data-stu-id="84841-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="84841-131">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84841-131">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-132">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="84841-132">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="84841-133">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="84841-133">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="84841-134">Use **NULL** para especificar que essa função não deve retornar até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="84841-134">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="84841-135">*ppEffectPool* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="84841-135">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-136">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="84841-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="84841-137">O endereço de um ponteiro para o pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="84841-137">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="84841-138">*ppErrors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="84841-138">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-139">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="84841-139">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="84841-140">O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.</span><span class="sxs-lookup"><span data-stu-id="84841-140">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="84841-141">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="84841-141">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84841-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="84841-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="84841-143">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="84841-143">A pointer to the return value.</span></span> <span data-ttu-id="84841-144">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="84841-144">May be **NULL**.</span></span> <span data-ttu-id="84841-145">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="84841-145">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84841-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84841-146">Return value</span></span>

<span data-ttu-id="84841-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84841-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84841-148">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="84841-148">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="84841-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="84841-149">Remarks</span></span>

<span data-ttu-id="84841-150">Este exemplo cria um pool de efeitos a partir do efeito usado no [exemplo de BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="84841-150">This example creates an effect pool from the effect used in the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a><span data-ttu-id="84841-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84841-151">Requirements</span></span>



| <span data-ttu-id="84841-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="84841-152">Requirement</span></span> | <span data-ttu-id="84841-153">Valor</span><span class="sxs-lookup"><span data-stu-id="84841-153">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84841-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84841-154">Header</span></span><br/> | <dl> <span data-ttu-id="84841-155"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="84841-155"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84841-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="84841-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84841-157">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="84841-157">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
