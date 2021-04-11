---
description: Salva um buffer de PRT (transferência radiante em cluster) compactado em disco.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Função D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930584"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a><span data-ttu-id="524fb-103">Função D3DXSavePRTCompBufferToFile</span><span class="sxs-lookup"><span data-stu-id="524fb-103">D3DXSavePRTCompBufferToFile function</span></span>

<span data-ttu-id="524fb-104">Salva um buffer de PRT (transferência radiante em cluster) compactado em disco.</span><span class="sxs-lookup"><span data-stu-id="524fb-104">Saves a compressed precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="524fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="524fb-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="524fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="524fb-106">Parameters</span></span>

<span data-ttu-id="524fb-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="524fb-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="524fb-108">Tipo: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="524fb-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="524fb-109">Nome do arquivo no qual o buffer compactado deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="524fb-109">Name of the file to which the compressed buffer is to be saved.</span></span>

<span data-ttu-id="524fb-110">*pBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="524fb-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="524fb-111">Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="524fb-111">Type: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span></span>

<span data-ttu-id="524fb-112">Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="524fb-112">Address of a pointer to the input [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="524fb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="524fb-113">Return value</span></span>

<span data-ttu-id="524fb-114">Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="524fb-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="524fb-115">Se o método for bem sucedido, o valor de retorno será **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="524fb-115">If the method succeeds, then the return value is **D3D\_OK**.</span></span> <span data-ttu-id="524fb-116">Se o método falhar, o valor de retorno poderá ser **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="524fb-116">If the method fails, then the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="524fb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="524fb-117">Remarks</span></span>

<span data-ttu-id="524fb-118">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="524fb-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="524fb-119">Se o Unicode estiver definido, a chamada de função será resolvida como [D3DXSavePRTCompBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="524fb-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTCompBufferToFileW]().</span></span> <span data-ttu-id="524fb-120">Caso contrário, a chamada de função será resolvida como **D3DXSavePRTCompBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="524fb-120">Otherwise, the function call resolves to **D3DXSavePRTCompBufferToFileA**.</span></span>

<span data-ttu-id="524fb-121">O formato de arquivo do PCA é um arquivo binário na forma de um cabeçalho e dois ou três blocos de dados.</span><span class="sxs-lookup"><span data-stu-id="524fb-121">The PCA file format is a binary file in the form of a header and then two or three data blocks.</span></span>

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

<span data-ttu-id="524fb-122">Para o caso de *bIsTex* ser diferente de zero, *NumSamples* deve ser igual `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="524fb-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="524fb-123">O bloco de dados base que segue o cabeçalho é de `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="524fb-123">The basis data block that follows the header is `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span></span>

<span data-ttu-id="524fb-124">Depois disso, está o bloco de dados de pesos do PCA, que é de `NumPCA * NumSamples * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="524fb-124">Following that is the PCA weights data block, which is `NumPCA * NumSamples * sizeof(float)` bytes.</span></span>

<span data-ttu-id="524fb-125">Se *NumClusters* for maior que 1, o arquivo terminará com o bloco de dados de IDs de cluster de `NumSamples * sizeof(UINT)` bytes.</span><span class="sxs-lookup"><span data-stu-id="524fb-125">If *NumClusters* is greater than 1, then the file ends with the cluster IDs data block of `NumSamples * sizeof(UINT)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="524fb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="524fb-126">Requirements</span></span>

| <span data-ttu-id="524fb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="524fb-127">Requirement</span></span> | <span data-ttu-id="524fb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="524fb-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="524fb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="524fb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="524fb-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="524fb-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="524fb-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="524fb-131">Library</span></span><br/> | <dl> <span data-ttu-id="524fb-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="524fb-132"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="524fb-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="524fb-133">See also</span></span>

[<span data-ttu-id="524fb-134">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="524fb-134">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
