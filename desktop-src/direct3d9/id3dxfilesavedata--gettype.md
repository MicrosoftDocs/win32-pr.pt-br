---
description: Recupera a ID do modelo deste nó de dados do arquivo.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'Método ID3DXFileSaveData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781197"
---
# <a name="id3dxfilesavedatagettype-method"></a><span data-ttu-id="91ba0-103">Método ID3DXFileSaveData:: GetType</span><span class="sxs-lookup"><span data-stu-id="91ba0-103">ID3DXFileSaveData::GetType method</span></span>

<span data-ttu-id="91ba0-104">Recupera a ID do modelo deste nó de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="91ba0-104">Retrieves the template ID of this file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ba0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91ba0-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a><span data-ttu-id="91ba0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91ba0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ba0-107">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="91ba0-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ba0-108">Tipo: **[ **GUID**](guid.md)\***</span><span class="sxs-lookup"><span data-stu-id="91ba0-108">Type: **[**GUID**](guid.md)\***</span></span>

<span data-ttu-id="91ba0-109">Ponteiro para o GUID que representa o modelo neste nó de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="91ba0-109">Pointer to the GUID representing the template in this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ba0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91ba0-110">Return value</span></span>

<span data-ttu-id="91ba0-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91ba0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91ba0-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91ba0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="91ba0-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="91ba0-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ba0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ba0-114">Requirements</span></span>



| <span data-ttu-id="91ba0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ba0-115">Requirement</span></span> | <span data-ttu-id="91ba0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="91ba0-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91ba0-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91ba0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="91ba0-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="91ba0-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="91ba0-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91ba0-119">Library</span></span><br/> | <dl> <span data-ttu-id="91ba0-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91ba0-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="91ba0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="91ba0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ba0-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="91ba0-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




