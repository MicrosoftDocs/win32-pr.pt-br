---
description: Recupera a ID do modelo neste objeto de dados de arquivo.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'Método ID3DXFileData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370985"
---
# <a name="id3dxfiledatagettype-method"></a><span data-ttu-id="d1c92-103">Método ID3DXFileData:: GetType</span><span class="sxs-lookup"><span data-stu-id="d1c92-103">ID3DXFileData::GetType method</span></span>

<span data-ttu-id="d1c92-104">Recupera a ID do modelo neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d1c92-104">Retrieves the template ID in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1c92-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a><span data-ttu-id="d1c92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c92-107">*pType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1c92-107">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c92-108">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="d1c92-108">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="d1c92-109">Ponteiro para o GUID que representa o modelo neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d1c92-109">Pointer to the GUID representing the template in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c92-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1c92-110">Return value</span></span>

<span data-ttu-id="d1c92-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1c92-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1c92-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1c92-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d1c92-113">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d1c92-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1c92-114">Requirements</span></span>



| <span data-ttu-id="d1c92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1c92-115">Requirement</span></span> | <span data-ttu-id="d1c92-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d1c92-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c92-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1c92-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d1c92-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c92-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d1c92-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1c92-119">Library</span></span><br/> | <dl> <span data-ttu-id="d1c92-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1c92-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d1c92-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1c92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c92-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="d1c92-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




