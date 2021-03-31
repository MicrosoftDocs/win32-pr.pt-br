---
description: Adiciona uma referência de dados como um filho deste nó de dados do arquivo ID3DXFileSaveData. A referência de dados aponta para um objeto de dados de arquivo.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'Método ID3DXFileSaveData:: AddDataReference (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930648"
---
# <a name="id3dxfilesavedataadddatareference-method"></a><span data-ttu-id="644c5-104">Método ID3DXFileSaveData:: AddDataReference</span><span class="sxs-lookup"><span data-stu-id="644c5-104">ID3DXFileSaveData::AddDataReference method</span></span>

<span data-ttu-id="644c5-105">Adiciona uma referência de dados como um filho deste nó de dados do arquivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="644c5-105">Adds a data reference as a child of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span> <span data-ttu-id="644c5-106">A referência de dados aponta para um objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="644c5-106">The data reference points to a file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="644c5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="644c5-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a><span data-ttu-id="644c5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="644c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="644c5-109">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="644c5-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="644c5-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="644c5-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="644c5-111">Ponteiro para o nome do objeto de dados a ser adicionado por referência.</span><span class="sxs-lookup"><span data-stu-id="644c5-111">Pointer to the name of the data object to add by reference.</span></span> <span data-ttu-id="644c5-112">Especifique **NULL** se o objeto de dados não tiver um nome.</span><span class="sxs-lookup"><span data-stu-id="644c5-112">Specify **NULL** if the data object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="644c5-113">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="644c5-113">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="644c5-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="644c5-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="644c5-115">Ponteiro para um GUID que representa o objeto de dados a ser adicionado por referência.</span><span class="sxs-lookup"><span data-stu-id="644c5-115">Pointer to a GUID representing the data object to add by reference.</span></span> <span data-ttu-id="644c5-116">Se for **NULL**, será adicionada uma referência que aponta para o objeto de dados com o nome fornecido por szName.</span><span class="sxs-lookup"><span data-stu-id="644c5-116">If **NULL**, a reference will be added that points to the data object with the name given by szName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="644c5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="644c5-117">Return value</span></span>

<span data-ttu-id="644c5-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="644c5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="644c5-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="644c5-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="644c5-120">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="644c5-120">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="644c5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="644c5-121">Remarks</span></span>

<span data-ttu-id="644c5-122">O objeto de dados de arquivo que está sendo referenciado deve ter um nome ou um GUID.</span><span class="sxs-lookup"><span data-stu-id="644c5-122">The file data object being referenced must have either a name or a GUID.</span></span> <span data-ttu-id="644c5-123">O objeto de dados de arquivo também deve derivar de um objeto pai [**ID3DXFileSaveData**](id3dxfilesavedata.md) diferente.</span><span class="sxs-lookup"><span data-stu-id="644c5-123">The file data object must also derive from a different parent [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="644c5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="644c5-124">Requirements</span></span>



| <span data-ttu-id="644c5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="644c5-125">Requirement</span></span> | <span data-ttu-id="644c5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="644c5-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="644c5-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="644c5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="644c5-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="644c5-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="644c5-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="644c5-129">Library</span></span><br/> | <dl> <span data-ttu-id="644c5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="644c5-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="644c5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="644c5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644c5-132">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="644c5-132">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
