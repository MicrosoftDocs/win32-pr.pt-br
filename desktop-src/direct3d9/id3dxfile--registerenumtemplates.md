---
description: Registra modelos personalizados, dado um objeto de enumeração ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'Método ID3DXFile:: RegisterEnumTemplates (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370980"
---
# <a name="id3dxfileregisterenumtemplates-method"></a><span data-ttu-id="d9061-103">Método ID3DXFile:: RegisterEnumTemplates</span><span class="sxs-lookup"><span data-stu-id="d9061-103">ID3DXFile::RegisterEnumTemplates method</span></span>

<span data-ttu-id="d9061-104">Registra modelos personalizados, dado um objeto de enumeração [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="d9061-104">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9061-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9061-105">Syntax</span></span>


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="d9061-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9061-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9061-107">*pEnum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9061-107">*pEnum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9061-108">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9061-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span></span>

<span data-ttu-id="d9061-109">Ponteiro para um objeto de enumeração [**ID3DXFileEnumObject**](id3dxfileenumobject.md) que contém modelos.</span><span class="sxs-lookup"><span data-stu-id="d9061-109">Pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object that contains templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9061-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9061-110">Return value</span></span>

<span data-ttu-id="d9061-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9061-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9061-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9061-112">If the method succeeds, the return value is S\_OK .</span></span>

<span data-ttu-id="d9061-113">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d9061-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9061-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9061-114">Remarks</span></span>

<span data-ttu-id="d9061-115">Quando esse método é chamado, ele copia modelos armazenados com o ID3DXFileEnumObject, representando o arquivo, para o repositório de modelos local do objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="d9061-115">When this method is called, it copies templates stored with the ID3DXFileEnumObject, representing the file, to the local template store of the [**ID3DXFile**](id3dxfile.md) object.</span></span>

<span data-ttu-id="d9061-116">Se um ponteiro [**ID3DXFileEnumObject**](id3dxfileenumobject.md) não estiver disponível, chame o método [**RegisterTemplates**](id3dxfile--registertemplates.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d9061-116">If an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pointer is not available, call the [**RegisterTemplates**](id3dxfile--registertemplates.md) method instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9061-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9061-117">Requirements</span></span>



| <span data-ttu-id="d9061-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9061-118">Requirement</span></span> | <span data-ttu-id="d9061-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d9061-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9061-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9061-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d9061-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9061-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d9061-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9061-122">Library</span></span><br/> | <dl> <span data-ttu-id="d9061-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9061-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d9061-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9061-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9061-125">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="d9061-125">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="d9061-126">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="d9061-126">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




