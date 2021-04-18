---
description: Salva um objeto de dados e seus filhos em um arquivo do DirectX. Preterido.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'Método IDirectXFileSaveObject:: SaveData (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791624"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a><span data-ttu-id="ebb4d-104">Método IDirectXFileSaveObject:: SaveData</span><span class="sxs-lookup"><span data-stu-id="ebb4d-104">IDirectXFileSaveObject::SaveData method</span></span>

<span data-ttu-id="ebb4d-105">Salva um objeto de dados e seus filhos em um arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="ebb4d-105">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="ebb4d-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="ebb4d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb4d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebb4d-107">Syntax</span></span>


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="ebb4d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebb4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb4d-109">*pDataObj* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ebb4d-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb4d-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="ebb4d-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="ebb4d-111">Ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , representando o objeto de dados de arquivo a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="ebb4d-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb4d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebb4d-112">Return value</span></span>

<span data-ttu-id="ebb4d-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebb4d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebb4d-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ebb4d-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ebb4d-115">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="ebb4d-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb4d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb4d-116">Requirements</span></span>



| <span data-ttu-id="ebb4d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb4d-117">Requirement</span></span> | <span data-ttu-id="ebb4d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ebb4d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb4d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebb4d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ebb4d-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebb4d-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebb4d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebb4d-121">Library</span></span><br/> | <dl> <span data-ttu-id="ebb4d-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebb4d-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebb4d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebb4d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb4d-124">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="ebb4d-124">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 




