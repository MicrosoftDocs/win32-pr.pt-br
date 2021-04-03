---
description: Cria uma instância de um objeto ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Função D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091967"
---
# <a name="d3dxfilecreate-function"></a><span data-ttu-id="34a2f-103">Função D3DXFileCreate</span><span class="sxs-lookup"><span data-stu-id="34a2f-103">D3DXFileCreate function</span></span>

<span data-ttu-id="34a2f-104">Cria uma instância de um objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="34a2f-104">Creates an instance of an [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34a2f-105">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="34a2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a2f-107">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="34a2f-107">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="34a2f-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="34a2f-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="34a2f-109">Endereço de um ponteiro para uma interface [**ID3DXFile**](id3dxfile.md) , que representa o objeto de arquivo. x criado.</span><span class="sxs-lookup"><span data-stu-id="34a2f-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the created .x file object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a2f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34a2f-110">Return value</span></span>

<span data-ttu-id="34a2f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34a2f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34a2f-112">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34a2f-112">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="34a2f-113">Se a função falhar, o valor de retorno poderá ser um dos seguintes: E \_ ponteiro, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="34a2f-113">If the function fails, the return value can be one of the following: E\_POINTER, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a2f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="34a2f-114">Remarks</span></span>

<span data-ttu-id="34a2f-115">Depois de usar essa função, use [**RegisterTemplates**](id3dxfile--registertemplates.md) ou [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) para registrar modelos, [**createenumobject**](id3dxfile--createenumobject.md) para criar um objeto enumerador ou [**createsaveobject**](id3dxfile--createsaveobject.md) para criar um objeto Save.</span><span class="sxs-lookup"><span data-stu-id="34a2f-115">After using this function, use [**RegisterTemplates**](id3dxfile--registertemplates.md) or [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) to register templates, [**CreateEnumObject**](id3dxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](id3dxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a2f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34a2f-116">Requirements</span></span>



| <span data-ttu-id="34a2f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="34a2f-117">Requirement</span></span> | <span data-ttu-id="34a2f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="34a2f-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34a2f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34a2f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="34a2f-120"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="34a2f-120"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="34a2f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34a2f-121">Library</span></span><br/> | <dl> <span data-ttu-id="34a2f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34a2f-122"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="34a2f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="34a2f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a2f-124">Funções de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="34a2f-124">D3DX X File Functions</span></span>](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="34a2f-125">**Createenumobject**</span><span class="sxs-lookup"><span data-stu-id="34a2f-125">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="34a2f-126">**Createsaveobject**</span><span class="sxs-lookup"><span data-stu-id="34a2f-126">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="34a2f-127">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="34a2f-127">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[<span data-ttu-id="34a2f-128">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="34a2f-128">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




