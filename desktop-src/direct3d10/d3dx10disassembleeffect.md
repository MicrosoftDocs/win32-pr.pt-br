---
description: Observação em vez de usar essa função herdada, recomendamos que você use a API D3DDisassemble. Essa função – que desmonta um efeito compilado em uma cadeia de texto que contém instruções de assembly e registra atribuições--foi preterida.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: Função D3DX10DisassembleEffect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930666"
---
# <a name="d3dx10disassembleeffect-function"></a><span data-ttu-id="edced-104">Função D3DX10DisassembleEffect</span><span class="sxs-lookup"><span data-stu-id="edced-104">D3DX10DisassembleEffect function</span></span>

> [!Note]  
> <span data-ttu-id="edced-105">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="edced-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="edced-106">Essa função – que desmonta um efeito compilado em uma cadeia de texto que contém instruções de assembly e registra atribuições--foi preterida.</span><span class="sxs-lookup"><span data-stu-id="edced-106">This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated.</span></span> <span data-ttu-id="edced-107">Em vez disso, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="edced-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="edced-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edced-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="edced-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edced-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edced-110">*pEffect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edced-110">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edced-111">Tipo: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span><span class="sxs-lookup"><span data-stu-id="edced-111">Type: **[**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span></span>

<span data-ttu-id="edced-112">Um ponteiro para a interface de efeito (consulte a [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span><span class="sxs-lookup"><span data-stu-id="edced-112">A pointer to the effect interface (see [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span></span>

</dd> <dt>

<span data-ttu-id="edced-113">*EnableColorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edced-113">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edced-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edced-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edced-115">Inclua marcas HTML na saída para codificar por cor o resultado.</span><span class="sxs-lookup"><span data-stu-id="edced-115">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="edced-116">*ppDisassembly* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="edced-116">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edced-117">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="edced-117">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="edced-118">Endereço de um buffer (consulte a [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o efeito desmontado.</span><span class="sxs-lookup"><span data-stu-id="edced-118">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edced-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edced-119">Return value</span></span>

<span data-ttu-id="edced-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="edced-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="edced-121">Retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="edced-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edced-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edced-122">Requirements</span></span>



| <span data-ttu-id="edced-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="edced-123">Requirement</span></span> | <span data-ttu-id="edced-124">Valor</span><span class="sxs-lookup"><span data-stu-id="edced-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edced-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="edced-125">Header</span></span><br/> | <dl> <span data-ttu-id="edced-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="edced-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edced-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="edced-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edced-128">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="edced-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
