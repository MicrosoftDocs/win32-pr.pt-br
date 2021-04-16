---
description: Observação em vez de usar essa função herdada, recomendamos que você use a API D3DDisassemble. Essa função – que desmonta um sombreador compilado em uma cadeia de texto que contém instruções de assembly e registros de atribuições--não existe mais.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: Função D3DX10DisassembleShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786958"
---
# <a name="d3dx10disassembleshader-function"></a><span data-ttu-id="a2515-104">Função D3DX10DisassembleShader</span><span class="sxs-lookup"><span data-stu-id="a2515-104">D3DX10DisassembleShader function</span></span>

> [!Note]  
> <span data-ttu-id="a2515-105">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="a2515-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="a2515-106">Essa função – que desmonta um sombreador compilado em uma cadeia de texto que contém instruções de assembly e registros de atribuições--não existe mais.</span><span class="sxs-lookup"><span data-stu-id="a2515-106">This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- no longer exists.</span></span> <span data-ttu-id="a2515-107">Em vez disso, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="a2515-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2515-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2515-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="a2515-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2515-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2515-110">*pShader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2515-110">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2515-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="a2515-111">Type: **const void\***</span></span>

<span data-ttu-id="a2515-112">Um ponteiro para o [**sombreador compilado**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="a2515-112">A pointer to the [**compiled shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="a2515-113">*BytecodeLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2515-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2515-114">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2515-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2515-115">O tamanho de pShader.</span><span class="sxs-lookup"><span data-stu-id="a2515-115">The size of pShader.</span></span>

</dd> <dt>

<span data-ttu-id="a2515-116">*EnableColorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2515-116">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2515-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2515-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2515-118">Inclua marcas HTML na saída para codificar por cor o resultado.</span><span class="sxs-lookup"><span data-stu-id="a2515-118">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="a2515-119">*pComments* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2515-119">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2515-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2515-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2515-121">A cadeia de caracteres de comentário na parte superior do sombreador que identifica as constantes e variáveis do sombreador.</span><span class="sxs-lookup"><span data-stu-id="a2515-121">The comment string at the top of the shader that identifies the shader constants and variables.</span></span>

</dd> <dt>

<span data-ttu-id="a2515-122">*ppDisassembly* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a2515-122">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2515-123">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a2515-123">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a2515-124">Endereço de um buffer (consulte a [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o sombreador desmontado.</span><span class="sxs-lookup"><span data-stu-id="a2515-124">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2515-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2515-125">Return value</span></span>

<span data-ttu-id="a2515-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2515-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2515-127">Retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a2515-127">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2515-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2515-128">Remarks</span></span>

<span data-ttu-id="a2515-129">Esse texto retornado inclui um cabeçalho com a versão do compilador HLSL usado para gerar esse objeto, comentários que descrevem o layout de memória dos buffers de constantes usados pelo sombreador, assinaturas de entrada e saída e pontos de associação de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2515-129">This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.</span></span>

<span data-ttu-id="a2515-130">Aqui está um exemplo de desmontagem de um sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="a2515-130">Here is an example of disassembling a compiled shader.</span></span> <span data-ttu-id="a2515-131">O exemplo pressupõe que você comece com um sombreador compilado (mostrado como *pVSBuf* , que pode ser visto no [exemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="a2515-131">The example assumes you start with a compiled shader (shown as *pVSBuf* which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="a2515-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2515-132">Requirements</span></span>



| <span data-ttu-id="a2515-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2515-133">Requirement</span></span> | <span data-ttu-id="a2515-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a2515-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2515-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2515-135">Header</span></span><br/> | <dl> <span data-ttu-id="a2515-136"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2515-136"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2515-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2515-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2515-138">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="a2515-138">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
