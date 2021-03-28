---
title: Registro float de constante (referência de HLSL VS)
description: Registro de entrada do sombreador de vértice para uma constante de ponto flutuante de quatro componentes. Defina um registro constante com def-vs ou SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366163"
---
# <a name="constant-float-register-hlsl-vs-reference"></a><span data-ttu-id="31407-104">Registro float de constante (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="31407-104">Constant float register (HLSL VS reference)</span></span>

<span data-ttu-id="31407-105">Registro de entrada do sombreador de vértice para uma constante de ponto flutuante de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="31407-105">Vertex shader input register for a four component floating-point constant.</span></span> <span data-ttu-id="31407-106">Defina um registro constante com [def-vs](def---vs.md) ou [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="31407-106">Set a constant register with either [def - vs](def---vs.md) or [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span></span>

<span data-ttu-id="31407-107">O arquivo de registro constante é somente leitura da perspectiva do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="31407-107">The constant register file is read-only from the perspective of the vertex shader.</span></span> <span data-ttu-id="31407-108">Qualquer instrução única pode acessar apenas um registro constante.</span><span class="sxs-lookup"><span data-stu-id="31407-108">Any single instruction may access only one constant register.</span></span> <span data-ttu-id="31407-109">No entanto, cada fonte nessa instrução pode Swizzler de forma independente e negar esse vetor conforme ele é lido.</span><span class="sxs-lookup"><span data-stu-id="31407-109">However, each source in that instruction may independently swizzle and negate that vector as it is read.</span></span>

<span data-ttu-id="31407-110">O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="31407-110">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="31407-111">Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="31407-111">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="31407-112">O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador.</span><span class="sxs-lookup"><span data-stu-id="31407-112">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="31407-113">Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global.</span><span class="sxs-lookup"><span data-stu-id="31407-113">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="31407-114">As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.</span><span class="sxs-lookup"><span data-stu-id="31407-114">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="31407-115">Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="31407-115">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="31407-116">Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.</span><span class="sxs-lookup"><span data-stu-id="31407-116">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

<span data-ttu-id="31407-117">Um registro constante é designado como absoluto ou relativo:</span><span class="sxs-lookup"><span data-stu-id="31407-117">A constant register is designated as either absolute or relative:</span></span>


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



<span data-ttu-id="31407-118">O registro constante pode ser lido, portanto, usando um índice absoluto ou com um índice relativo de um registro de endereço.</span><span class="sxs-lookup"><span data-stu-id="31407-118">The constant register can be read, therefore, either by using an absolute index or with a relative index from an address register.</span></span> <span data-ttu-id="31407-119">Leituras de registros fora do intervalo retornam (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="31407-119">Reads from out-of-range registers return (0.0, 0.0, 0.0, 0.0).</span></span>

## <a name="examples"></a><span data-ttu-id="31407-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31407-120">Examples</span></span>

<span data-ttu-id="31407-121">Aqui está um exemplo declarando duas constantes de ponto flutuante em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="31407-121">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="31407-122">Essas constantes são carregadas toda vez que [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) é chamado.</span><span class="sxs-lookup"><span data-stu-id="31407-122">These constants are loaded every time [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) is called.</span></span>

<span data-ttu-id="31407-123">Aqui está um exemplo de uso da API.</span><span class="sxs-lookup"><span data-stu-id="31407-123">Here is an example using the API.</span></span>


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



<span data-ttu-id="31407-124">Se você estiver definindo valores constantes com a API, não haverá nenhuma declaração de sombreador necessária.</span><span class="sxs-lookup"><span data-stu-id="31407-124">If you are setting constant values with the API, there is no shader declaration required.</span></span>



| <span data-ttu-id="31407-125">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="31407-125">Vertex shader versions</span></span> | <span data-ttu-id="31407-126">1\_1</span><span class="sxs-lookup"><span data-stu-id="31407-126">1\_1</span></span> | <span data-ttu-id="31407-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31407-127">2\_0</span></span> | <span data-ttu-id="31407-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31407-128">2\_sw</span></span> | <span data-ttu-id="31407-129">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31407-129">2\_x</span></span> | <span data-ttu-id="31407-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31407-130">3\_0</span></span> | <span data-ttu-id="31407-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31407-131">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="31407-132">Registro constante</span><span class="sxs-lookup"><span data-stu-id="31407-132">Constant Register</span></span>      | <span data-ttu-id="31407-133">x</span><span class="sxs-lookup"><span data-stu-id="31407-133">x</span></span>    | <span data-ttu-id="31407-134">x</span><span class="sxs-lookup"><span data-stu-id="31407-134">x</span></span>    | <span data-ttu-id="31407-135">x</span><span class="sxs-lookup"><span data-stu-id="31407-135">x</span></span>     | <span data-ttu-id="31407-136">x</span><span class="sxs-lookup"><span data-stu-id="31407-136">x</span></span>    | <span data-ttu-id="31407-137">x</span><span class="sxs-lookup"><span data-stu-id="31407-137">x</span></span>    | <span data-ttu-id="31407-138">x</span><span class="sxs-lookup"><span data-stu-id="31407-138">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="31407-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31407-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31407-140">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="31407-140">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 