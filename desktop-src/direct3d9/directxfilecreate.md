---
description: Cria uma instância de um objeto DirectXfile. Preterido.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Função DirectXFileCreate (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793992"
---
# <a name="directxfilecreate-function"></a><span data-ttu-id="d8864-104">Função DirectXFileCreate</span><span class="sxs-lookup"><span data-stu-id="d8864-104">DirectXFileCreate function</span></span>

<span data-ttu-id="d8864-105">Cria uma instância de um objeto DirectXfile.</span><span class="sxs-lookup"><span data-stu-id="d8864-105">Creates an instance of a DirectXFile object.</span></span> <span data-ttu-id="d8864-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="d8864-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8864-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8864-107">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="d8864-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8864-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8864-109">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="d8864-109">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="d8864-110">Tipo: **[ **LPDIRECTXFILE**](idirectxfile.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8864-110">Type: **[**LPDIRECTXFILE**](idirectxfile.md)\***</span></span>

<span data-ttu-id="d8864-111">Endereço de um ponteiro para uma interface [**IDirectXFile**](idirectxfile.md) , que representa o objeto directxfile criado.</span><span class="sxs-lookup"><span data-stu-id="d8864-111">Address of a pointer to an [**IDirectXFile**](idirectxfile.md) interface, representing the created DirectXFile object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8864-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8864-112">Return value</span></span>

<span data-ttu-id="d8864-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8864-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8864-114">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8864-114">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8864-115">Se a função falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d8864-115">If the function fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8864-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8864-116">Remarks</span></span>

<span data-ttu-id="d8864-117">Depois de usar essa função, use [**RegisterTemplates**](idirectxfile--registertemplates.md) para registrar modelos, [**createenumobject**](idirectxfile--createenumobject.md) para criar um objeto enumerador ou [**createsaveobject**](idirectxfile--createsaveobject.md) para criar um objeto Save.</span><span class="sxs-lookup"><span data-stu-id="d8864-117">After using this function, use [**RegisterTemplates**](idirectxfile--registertemplates.md) to register templates, [**CreateEnumObject**](idirectxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](idirectxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8864-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8864-118">Requirements</span></span>



| <span data-ttu-id="d8864-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8864-119">Requirement</span></span> | <span data-ttu-id="d8864-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d8864-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8864-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8864-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d8864-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8864-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8864-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8864-123">Library</span></span><br/> | <dl> <span data-ttu-id="d8864-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8864-124"><dt>D3dxof.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8864-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d8864-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8864-126"><dt>D3dxof.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8864-126"><dt>D3dxof.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8864-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8864-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8864-128">Funções de arquivo X</span><span class="sxs-lookup"><span data-stu-id="d8864-128">X File Functions</span></span>](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="d8864-129">**Createenumobject**</span><span class="sxs-lookup"><span data-stu-id="d8864-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="d8864-130">**Createsaveobject**</span><span class="sxs-lookup"><span data-stu-id="d8864-130">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="d8864-131">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="d8864-131">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




