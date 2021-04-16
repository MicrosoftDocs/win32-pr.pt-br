---
description: Cria e adiciona um objeto de referência de dados como um objeto filho. Preterido.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Método IDirectXFileData:: AddDataReference (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765314"
---
# <a name="idirectxfiledataadddatareference-method"></a><span data-ttu-id="3a94e-104">Método IDirectXFileData:: AddDataReference</span><span class="sxs-lookup"><span data-stu-id="3a94e-104">IDirectXFileData::AddDataReference method</span></span>

<span data-ttu-id="3a94e-105">Cria e adiciona um objeto de referência de dados como um objeto filho.</span><span class="sxs-lookup"><span data-stu-id="3a94e-105">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="3a94e-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3a94e-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a94e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a94e-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a><span data-ttu-id="3a94e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a94e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a94e-109">*szRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a94e-109">*szRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a94e-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a94e-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a94e-111">Ponteiro para o nome do objeto de dados referenciado.</span><span class="sxs-lookup"><span data-stu-id="3a94e-111">Pointer to the name of the referenced data object.</span></span> <span data-ttu-id="3a94e-112">Esse parâmetro poderá ser **nulo** se pguidRef fornecer uma referência para o GUID.</span><span class="sxs-lookup"><span data-stu-id="3a94e-112">This parameter can be **NULL** if pguidRef provides a reference to the GUID.</span></span>

</dd> <dt>

<span data-ttu-id="3a94e-113">*pguidRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a94e-113">*pguidRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a94e-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="3a94e-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="3a94e-115">Ponteiro para o GUID que representa os dados.</span><span class="sxs-lookup"><span data-stu-id="3a94e-115">Pointer to the GUID representing the data.</span></span> <span data-ttu-id="3a94e-116">Esse parâmetro poderá ser **nulo** se szRef fornecer uma referência ao nome.</span><span class="sxs-lookup"><span data-stu-id="3a94e-116">This parameter can be **NULL** if szRef provides a reference to the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a94e-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a94e-117">Return value</span></span>

<span data-ttu-id="3a94e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a94e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a94e-119">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a94e-119">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3a94e-120">Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="3a94e-120">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="3a94e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a94e-121">Remarks</span></span>

<span data-ttu-id="3a94e-122">Para que esse método tenha sucesso, o parâmetro szRef ou pguidRef deve ser não **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3a94e-122">For this method to succeed, either the szRef or pguidRef parameter must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a94e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a94e-123">Requirements</span></span>



| <span data-ttu-id="3a94e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a94e-124">Requirement</span></span> | <span data-ttu-id="3a94e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3a94e-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a94e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a94e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3a94e-127"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a94e-127"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a94e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a94e-128">Library</span></span><br/> | <dl> <span data-ttu-id="3a94e-129"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a94e-129"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a94e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a94e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a94e-131">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="3a94e-131">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 
