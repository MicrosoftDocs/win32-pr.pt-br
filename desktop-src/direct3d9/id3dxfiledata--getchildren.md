---
description: Recupera o número de filhos neste objeto de dados de arquivo.
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'Método ID3DXFileData:: GetChildren (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dd6932801f3d4b079efa6f1ed2688505dbd7828b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811259"
---
# <a name="id3dxfiledatagetchildren-method"></a><span data-ttu-id="93bd1-103">Método ID3DXFileData:: GetChildren</span><span class="sxs-lookup"><span data-stu-id="93bd1-103">ID3DXFileData::GetChildren method</span></span>

<span data-ttu-id="93bd1-104">Recupera o número de filhos neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="93bd1-104">Retrieves the number of children in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bd1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93bd1-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="93bd1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93bd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bd1-107">*puiChildren* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93bd1-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bd1-108">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="93bd1-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="93bd1-109">Endereço de um ponteiro para receber o número de filhos neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="93bd1-109">Address of a pointer to receive the number of children in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bd1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93bd1-110">Return value</span></span>

<span data-ttu-id="93bd1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93bd1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93bd1-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93bd1-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="93bd1-113">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="93bd1-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="93bd1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93bd1-114">Requirements</span></span>



| <span data-ttu-id="93bd1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="93bd1-115">Requirement</span></span> | <span data-ttu-id="93bd1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="93bd1-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93bd1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93bd1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="93bd1-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="93bd1-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="93bd1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93bd1-119">Library</span></span><br/> | <dl> <span data-ttu-id="93bd1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93bd1-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="93bd1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="93bd1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bd1-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="93bd1-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
