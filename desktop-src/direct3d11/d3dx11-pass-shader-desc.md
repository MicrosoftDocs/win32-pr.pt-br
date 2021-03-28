---
title: Estrutura de D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Descreve uma passagem de efeito.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- Estrutura D3DX11_PASS_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968690"
---
# <a name="d3dx11_pass_shader_desc-structure"></a><span data-ttu-id="45a86-104">\_Estrutura desc de D3DX11 Pass \_ Shader \_</span><span class="sxs-lookup"><span data-stu-id="45a86-104">D3DX11\_PASS\_SHADER\_DESC structure</span></span>

<span data-ttu-id="45a86-105">Descreve uma passagem de efeito.</span><span class="sxs-lookup"><span data-stu-id="45a86-105">Describes an effect pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a86-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45a86-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="45a86-107">Membros</span><span class="sxs-lookup"><span data-stu-id="45a86-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="45a86-108">**pShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="45a86-108">**pShaderVariable**</span></span>
</dt> <dd>

<span data-ttu-id="45a86-109">Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="45a86-109">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="45a86-110">A variável da qual este sombreador veio.</span><span class="sxs-lookup"><span data-stu-id="45a86-110">The variable that this shader came from.</span></span>

</dd> <dt>

<span data-ttu-id="45a86-111">**ShaderIndex**</span><span class="sxs-lookup"><span data-stu-id="45a86-111">**ShaderIndex**</span></span>
</dt> <dd>

<span data-ttu-id="45a86-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45a86-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="45a86-113">O elemento de pShaderVariable (se for uma matriz) ou 0 se não for aplicável.</span><span class="sxs-lookup"><span data-stu-id="45a86-113">The element of pShaderVariable (if an array) or 0 if not applicable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45a86-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="45a86-114">Remarks</span></span>

<span data-ttu-id="45a86-115">O D3DX11 \_ Pass \_ Shader \_ DESC é usado com os métodos [**ID3DX11EffectPass**](id3dx11effectpass.md) get \* ShaderDesc.</span><span class="sxs-lookup"><span data-stu-id="45a86-115">D3DX11\_PASS\_SHADER\_DESC is used with [**ID3DX11EffectPass**](id3dx11effectpass.md) Get\*ShaderDesc methods.</span></span>

<span data-ttu-id="45a86-116">Se for uma atribuição de sombreador embutido, a interface retornada será uma variável de sombreador anônima, que não será recuperável de nenhuma outra maneira.</span><span class="sxs-lookup"><span data-stu-id="45a86-116">If this is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.</span></span> <span data-ttu-id="45a86-117">Seu nome na variável descrição será "$Anonymous".</span><span class="sxs-lookup"><span data-stu-id="45a86-117">It's name in the variable description will be "$Anonymous".</span></span> <span data-ttu-id="45a86-118">Se não houver nenhuma atribuição desse tipo no bloco Pass, pShaderVariable! = **NULL**, mas pShaderVariable->IsValid () = = **false**.</span><span class="sxs-lookup"><span data-stu-id="45a86-118">If there is no assignment of this type in the pass block, pShaderVariable != **NULL**, but pShaderVariable->IsValid() == **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="45a86-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45a86-119">Requirements</span></span>



| <span data-ttu-id="45a86-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45a86-120">Requirement</span></span> | <span data-ttu-id="45a86-121">Valor</span><span class="sxs-lookup"><span data-stu-id="45a86-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="45a86-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45a86-122">Header</span></span><br/> | <dl> <span data-ttu-id="45a86-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="45a86-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45a86-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="45a86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a86-125">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="45a86-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

