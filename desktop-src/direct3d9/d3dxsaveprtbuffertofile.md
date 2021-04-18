---
description: Salva um buffer de PRT (transferência de radiante de computação) em disco.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Função D3DXSavePRTBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105759865"
---
# <a name="d3dxsaveprtbuffertofile-function"></a><span data-ttu-id="3284f-103">Função D3DXSavePRTBufferToFile</span><span class="sxs-lookup"><span data-stu-id="3284f-103">D3DXSavePRTBufferToFile function</span></span>

<span data-ttu-id="3284f-104">Salva um buffer de PRT (transferência de radiante de computação) em disco.</span><span class="sxs-lookup"><span data-stu-id="3284f-104">Saves a precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="3284f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3284f-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="3284f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3284f-106">Parameters</span></span>

<span data-ttu-id="3284f-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3284f-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="3284f-108">Tipo: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3284f-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3284f-109">Nome do arquivo no qual o buffer deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="3284f-109">Name of the file to which the buffer is to be saved.</span></span>

<span data-ttu-id="3284f-110">*pBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3284f-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="3284f-111">Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3284f-111">Type: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3284f-112">Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="3284f-112">Address of a pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="3284f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3284f-113">Return value</span></span>

<span data-ttu-id="3284f-114">Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="3284f-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="3284f-115">Se o método for bem sucedido, o valor de retorno será **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3284f-115">If the method succeeds, the return value is **D3D\_OK**.</span></span> <span data-ttu-id="3284f-116">Se o método falhar, o valor de retorno poderá ser **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="3284f-116">If the method fails, the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3284f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3284f-117">Remarks</span></span>

<span data-ttu-id="3284f-118">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="3284f-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3284f-119">Se o Unicode estiver definido, a chamada de função será resolvida como [D3DXSavePRTBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="3284f-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTBufferToFileW]().</span></span> <span data-ttu-id="3284f-120">Caso contrário, a chamada de função será resolvida como **D3DXSavePRTBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="3284f-120">Otherwise, the function call resolves to **D3DXSavePRTBufferToFileA**.</span></span>

<span data-ttu-id="3284f-121">O formato de arquivo PRT é um arquivo binário na forma de um cabeçalho e em um bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="3284f-121">The PRT file format is a binary file in the form of a header and then a data block.</span></span>

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

<span data-ttu-id="3284f-122">Para o caso de *bIsTex* ser diferente de zero, *NumSamples* deve ser igual `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="3284f-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="3284f-123">O bloco de dados que segue o cabeçalho é de `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="3284f-123">The data block that follows the header is `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3284f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3284f-124">Requirements</span></span>

| <span data-ttu-id="3284f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3284f-125">Requirement</span></span> | <span data-ttu-id="3284f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3284f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3284f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3284f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3284f-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3284f-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3284f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3284f-129">Library</span></span><br/> | <dl> <span data-ttu-id="3284f-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3284f-130"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="3284f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3284f-131">See also</span></span>

[<span data-ttu-id="3284f-132">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="3284f-132">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
