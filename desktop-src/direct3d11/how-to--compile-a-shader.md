---
title: Como compilar um sombreador
description: Este tópico mostra como usar a função D3DCompileFromFile em tempo de execução para compilar o código de sombreador.
ms.assetid: A2CE368F-E72A-453D-BA4D-3D1D53DDDEE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5eadb1d6627f553a9d769e6a0f43ab3ebe3a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641458"
---
# <a name="how-to-compile-a-shader"></a><span data-ttu-id="538f2-103">Como: compilar um sombreador</span><span class="sxs-lookup"><span data-stu-id="538f2-103">How To: Compile a Shader</span></span>

<span data-ttu-id="538f2-104">Normalmente, você usa o compilador de código do [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL como parte do processo de compilação para compilar o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="538f2-104">You typically use the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler as part of the build process to compile shader code.</span></span> <span data-ttu-id="538f2-105">Para obter mais informações sobre isso, consulte [compilando sombreadores](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-part1).</span><span class="sxs-lookup"><span data-stu-id="538f2-105">For more info about this, see [Compiling Shaders](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-part1).</span></span> <span data-ttu-id="538f2-106">Este tópico mostra como usar a função [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) em tempo de execução para compilar o código de sombreador.</span><span class="sxs-lookup"><span data-stu-id="538f2-106">This topic shows how to use the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) function at run time to compile shader code.</span></span>

<span data-ttu-id="538f2-107">**Para compilar um sombreador:**</span><span class="sxs-lookup"><span data-stu-id="538f2-107">**To compile a shader:**</span></span>

-   <span data-ttu-id="538f2-108">Compile o código do sombreador HLSL chamando [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="538f2-108">Compile HLSL shader code by calling [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile).</span></span>
    ```C++
        UINT flags = D3DCOMPILE_ENABLE_STRICTNESS;
    #if defined( DEBUG ) || defined( _DEBUG )
        flags |= D3DCOMPILE_DEBUG;
    #endif
        // Prefer higher CS shader profile when possible as CS 5.0 provides better performance on 11-class hardware.
        LPCSTR profile = ( device->GetFeatureLevel() >= D3D_FEATURE_LEVEL_11_0 ) ? "cs_5_0" : "cs_4_0";
        const D3D_SHADER_MACRO defines[] = 
        {
            "EXAMPLE_DEFINE", "1",
            NULL, NULL
        };
        ID3DBlob* shaderBlob = nullptr;
        ID3DBlob* errorBlob = nullptr;
        HRESULT hr = D3DCompileFromFile( srcFile, defines, D3D_COMPILE_STANDARD_FILE_INCLUDE,
                                         entryPoint, profile,
                                         flags, 0, &shaderBlob, &errorBlob );
    ```

    

<span data-ttu-id="538f2-109">O exemplo de código a seguir mostra como compilar vários sombreadores.</span><span class="sxs-lookup"><span data-stu-id="538f2-109">The following code example shows how to compile various shaders.</span></span>

> [!Note]  
> <span data-ttu-id="538f2-110">Para este código de exemplo, você precisa do SDK do Windows 8,0 e do \_ arquivo d3dcompiler44.dll da pasta% Program \_ File% \\ Windows kits \\ 8,0 \\ Redist \\ D3D \\ <arch> em seu caminho.</span><span class="sxs-lookup"><span data-stu-id="538f2-110">For this example code, you need the Windows SDK 8.0 and the d3dcompiler\_44.dll file from the %PROGRAM\_FILE%\\Windows Kits\\8.0\\Redist\\D3D\\<arch> folder in your path.</span></span> <span data-ttu-id="538f2-111">Os aplicativos da Windows Store dão suporte à compilação de tempo de execução para desenvolvimento, mas não para implantação.</span><span class="sxs-lookup"><span data-stu-id="538f2-111">Windows Store apps support run time compilation for development but not for deployment.</span></span>

 


```C++
#define _WIN32_WINNT 0x600
#include <stdio.h>

#include <d3dcompiler.h>

#pragma comment(lib,"d3dcompiler.lib")

HRESULT CompileShader( _In_ LPCWSTR srcFile, _In_ LPCSTR entryPoint, _In_ LPCSTR profile, _Outptr_ ID3DBlob** blob )
{
    if ( !srcFile || !entryPoint || !profile || !blob )
       return E_INVALIDARG;

    *blob = nullptr;

    UINT flags = D3DCOMPILE_ENABLE_STRICTNESS;
#if defined( DEBUG ) || defined( _DEBUG )
    flags |= D3DCOMPILE_DEBUG;
#endif

    const D3D_SHADER_MACRO defines[] = 
    {
        "EXAMPLE_DEFINE", "1",
        NULL, NULL
    };

    ID3DBlob* shaderBlob = nullptr;
    ID3DBlob* errorBlob = nullptr;
    HRESULT hr = D3DCompileFromFile( srcFile, defines, D3D_COMPILE_STANDARD_FILE_INCLUDE,
                                     entryPoint, profile,
                                     flags, 0, &shaderBlob, &errorBlob );
    if ( FAILED(hr) )
    {
        if ( errorBlob )
        {
            OutputDebugStringA( (char*)errorBlob->GetBufferPointer() );
            errorBlob->Release();
        }

        if ( shaderBlob )
           shaderBlob->Release();

        return hr;
    }    

    *blob = shaderBlob;

    return hr;
}

int main()
{
    // Compile vertex shader shader
    ID3DBlob *vsBlob = nullptr;
    HRESULT hr = CompileShader( L"BasicHLSL11_VS.hlsl", "VSMain", "vs_4_0_level_9_1", &vsBlob );
    if ( FAILED(hr) )
    {
        printf("Failed compiling vertex shader %08X\n", hr );
        return -1;
    }

    // Compile pixel shader shader
    ID3DBlob *psBlob = nullptr;
    hr = CompileShader( L"BasicHLSL11_PS.hlsl", "PSMain", "ps_4_0_level_9_1", &psBlob );
    if ( FAILED(hr) )
    {
        vsBlob->Release();
        printf("Failed compiling pixel shader %08X\n", hr );
        return -1;
    }

    printf("Success\n");

    // Clean up
    vsBlob->Release();
    psBlob->Release();

    return 0;
}

```



<span data-ttu-id="538f2-112">O exemplo de código anterior compila os blocos de código de sombreador de pixel e Vertex nos \_ arquivos BasicHLSL11 PS. HLSL e BasicHLSL11 \_ vs. HLSL.</span><span class="sxs-lookup"><span data-stu-id="538f2-112">The preceding code example compiles the pixel and vertex shader code blocks in the BasicHLSL11\_PS.hlsl and BasicHLSL11\_VS.hlsl files.</span></span> <span data-ttu-id="538f2-113">Aqui está o código em BasicHLSL11 \_ PS. HLSL:</span><span class="sxs-lookup"><span data-stu-id="538f2-113">Here is the code in BasicHLSL11\_PS.hlsl:</span></span>


```hlsl
//--------------------------------------------------------------------------------------
// File: BasicHLSL11_PS.hlsl
//
// The pixel shader file for the BasicHLSL11 sample.  
// 
// Copyright (c) Microsoft Corporation. All rights reserved.
//--------------------------------------------------------------------------------------

//--------------------------------------------------------------------------------------
// Globals
//--------------------------------------------------------------------------------------
cbuffer cbPerObject : register( b0 )
{
    float4        g_vObjectColor            : packoffset( c0 );
};

cbuffer cbPerFrame : register( b1 )
{
    float3        g_vLightDir                : packoffset( c0 );
    float        g_fAmbient                : packoffset( c0.w );
};

//--------------------------------------------------------------------------------------
// Textures and Samplers
//--------------------------------------------------------------------------------------
Texture2D    g_txDiffuse : register( t0 );
SamplerState g_samLinear : register( s0 );

//--------------------------------------------------------------------------------------
// Input / Output structures
//--------------------------------------------------------------------------------------
struct PS_INPUT
{
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
};

//--------------------------------------------------------------------------------------
// Pixel Shader
//--------------------------------------------------------------------------------------
float4 PSMain( PS_INPUT Input ) : SV_TARGET
{
    float4 vDiffuse = g_txDiffuse.Sample( g_samLinear, Input.vTexcoord );
    
    float fLighting = saturate( dot( g_vLightDir, Input.vNormal ) );
    fLighting = max( fLighting, g_fAmbient );
    
    return vDiffuse * fLighting;
}
```



<span data-ttu-id="538f2-114">Aqui está o código em BasicHLSL11 \_ vs. HLSL:</span><span class="sxs-lookup"><span data-stu-id="538f2-114">Here is the code in BasicHLSL11\_VS.hlsl:</span></span>


```hlsl
//--------------------------------------------------------------------------------------
// File: BasicHLSL11_VS.hlsl
//
// The vertex shader file for the BasicHLSL11 sample.  
// 
// Copyright (c) Microsoft Corporation. All rights reserved.
//--------------------------------------------------------------------------------------

//--------------------------------------------------------------------------------------
// Globals
//--------------------------------------------------------------------------------------
cbuffer cbPerObject : register( b0 )
{
    matrix        g_mWorldViewProjection    : packoffset( c0 );
    matrix        g_mWorld                : packoffset( c4 );
};

//--------------------------------------------------------------------------------------
// Input / Output structures
//--------------------------------------------------------------------------------------
struct VS_INPUT
{
    float4 vPosition    : POSITION;
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
};

struct VS_OUTPUT
{
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
    float4 vPosition    : SV_POSITION;
};

//--------------------------------------------------------------------------------------
// Vertex Shader
//--------------------------------------------------------------------------------------
VS_OUTPUT VSMain( VS_INPUT Input )
{
    VS_OUTPUT Output;
    
    Output.vPosition = mul( Input.vPosition, g_mWorldViewProjection );
    Output.vNormal = mul( Input.vNormal, (float3x3)g_mWorld );
    Output.vTexcoord = Input.vTexcoord;
    
    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="538f2-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="538f2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="538f2-116">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="538f2-116">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 