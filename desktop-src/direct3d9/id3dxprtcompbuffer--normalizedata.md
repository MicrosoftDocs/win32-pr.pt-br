---
description: Normaliza todos os pesos do PCA (análise de componente principal) para que fiquem entre-1 e 1. Os vetores de base são modificados para refletir essa normalização.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'Método ID3DXPRTCompBuffer:: NormalizeData (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791263"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a><span data-ttu-id="15219-104">Método ID3DXPRTCompBuffer:: NormalizeData</span><span class="sxs-lookup"><span data-stu-id="15219-104">ID3DXPRTCompBuffer::NormalizeData method</span></span>

<span data-ttu-id="15219-105">Normaliza todos os pesos do PCA (análise de componente principal) para que fiquem entre-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="15219-105">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="15219-106">Os vetores de base são modificados para refletir essa normalização.</span><span class="sxs-lookup"><span data-stu-id="15219-106">Basis vectors are modified to reflect this normalization.</span></span>

## <a name="syntax"></a><span data-ttu-id="15219-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15219-107">Syntax</span></span>


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a><span data-ttu-id="15219-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15219-108">Parameters</span></span>

<span data-ttu-id="15219-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15219-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15219-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15219-110">Return value</span></span>

<span data-ttu-id="15219-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15219-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15219-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15219-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="15219-113">Se o método falhar, o valor a seguir será retornado.</span><span class="sxs-lookup"><span data-stu-id="15219-113">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="15219-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15219-114">Requirements</span></span>



| <span data-ttu-id="15219-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="15219-115">Requirement</span></span> | <span data-ttu-id="15219-116">Valor</span><span class="sxs-lookup"><span data-stu-id="15219-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15219-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15219-117">Header</span></span><br/>  | <dl> <span data-ttu-id="15219-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="15219-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="15219-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15219-119">Library</span></span><br/> | <dl> <span data-ttu-id="15219-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15219-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15219-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="15219-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15219-122">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="15219-122">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




