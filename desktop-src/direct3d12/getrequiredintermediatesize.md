---
title: Função GetRequiredIntermediateSize (D3dx12. h)
description: Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- Função GetRequiredIntermediateSize
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752179"
---
# <a name="getrequiredintermediatesize-function"></a><span data-ttu-id="40a0e-104">Função GetRequiredIntermediateSize</span><span class="sxs-lookup"><span data-stu-id="40a0e-104">GetRequiredIntermediateSize function</span></span>

<span data-ttu-id="40a0e-105">Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados.</span><span class="sxs-lookup"><span data-stu-id="40a0e-105">Returns the required size of a buffer to be used for data upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a0e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40a0e-106">Syntax</span></span>


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a><span data-ttu-id="40a0e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40a0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a0e-108">*pDestinationResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40a0e-108">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a0e-109">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="40a0e-109">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="40a0e-110">Um ponteiro para a interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="40a0e-110">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="40a0e-111">*FirstSubresource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40a0e-111">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a0e-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40a0e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40a0e-113">O índice do primeiro subrecurso no recurso.</span><span class="sxs-lookup"><span data-stu-id="40a0e-113">The index of the first subresource in the resource.</span></span> <span data-ttu-id="40a0e-114">O intervalo de valores válidos é de 0 a D3D12 \_ req \_ subrecursos.</span><span class="sxs-lookup"><span data-stu-id="40a0e-114">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="40a0e-115">*NumSubresources* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40a0e-115">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a0e-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40a0e-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40a0e-117">O número de subrecursos no recurso.</span><span class="sxs-lookup"><span data-stu-id="40a0e-117">The number of subresources in the resource.</span></span> <span data-ttu-id="40a0e-118">O intervalo de valores válidos é de 0 a (D3D12 \_ req \_ subresources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="40a0e-118">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a0e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40a0e-119">Return value</span></span>

<span data-ttu-id="40a0e-120">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40a0e-120">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="40a0e-121">O tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="40a0e-121">The size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a0e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40a0e-122">Requirements</span></span>



| <span data-ttu-id="40a0e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a0e-123">Requirement</span></span> | <span data-ttu-id="40a0e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="40a0e-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40a0e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40a0e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="40a0e-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a0e-126"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="40a0e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40a0e-127">Library</span></span><br/> | <dl> <span data-ttu-id="40a0e-128"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40a0e-128"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="40a0e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="40a0e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="40a0e-130"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40a0e-130"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a0e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="40a0e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a0e-132">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="40a0e-132">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

