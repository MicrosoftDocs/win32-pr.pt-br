---
description: Recupera um objeto filho neste objeto de dados de arquivo.
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'Método ID3DXFileData:: GetChild (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 37982ca1e4801b7d70bec503ff9510fc66772651
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930654"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="d76b8-103">Método ID3DXFileData:: GetChild</span><span class="sxs-lookup"><span data-stu-id="d76b8-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="d76b8-104">Recupera um objeto filho neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d76b8-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d76b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d76b8-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="d76b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d76b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76b8-107">*uiChild* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d76b8-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76b8-108">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d76b8-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d76b8-109">ID do objeto filho a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="d76b8-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d76b8-110">*ppChild* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d76b8-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76b8-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d76b8-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="d76b8-112">Endereço de um ponteiro para receber o ponteiro de interface do objeto filho.</span><span class="sxs-lookup"><span data-stu-id="d76b8-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76b8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d76b8-113">Return value</span></span>

<span data-ttu-id="d76b8-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d76b8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d76b8-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d76b8-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d76b8-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="d76b8-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="d76b8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d76b8-117">Requirements</span></span>



| <span data-ttu-id="d76b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d76b8-118">Requirement</span></span> | <span data-ttu-id="d76b8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d76b8-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d76b8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d76b8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d76b8-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d76b8-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d76b8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d76b8-122">Library</span></span><br/> | <dl> <span data-ttu-id="d76b8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d76b8-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d76b8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d76b8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76b8-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="d76b8-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
