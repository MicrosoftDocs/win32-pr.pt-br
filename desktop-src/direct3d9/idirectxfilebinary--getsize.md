---
description: Recupera o tamanho dos dados binários. Preterido.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'Método IDirectXFileBinary:: GetSize (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506511"
---
# <a name="idirectxfilebinarygetsize-method"></a><span data-ttu-id="0a45d-104">Método IDirectXFileBinary:: GetSize</span><span class="sxs-lookup"><span data-stu-id="0a45d-104">IDirectXFileBinary::GetSize method</span></span>

<span data-ttu-id="0a45d-105">Recupera o tamanho dos dados binários.</span><span class="sxs-lookup"><span data-stu-id="0a45d-105">Retrieves the size of the binary data.</span></span> <span data-ttu-id="0a45d-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="0a45d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a45d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a45d-107">Syntax</span></span>


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="0a45d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a45d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a45d-109">*pcbSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0a45d-109">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a45d-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a45d-110">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0a45d-111">Ponteiro para o tamanho retornado dos dados binários, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0a45d-111">Pointer to the returned size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a45d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a45d-112">Return value</span></span>

<span data-ttu-id="0a45d-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a45d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a45d-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a45d-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="0a45d-115">Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="0a45d-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a45d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a45d-116">Requirements</span></span>



| <span data-ttu-id="0a45d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a45d-117">Requirement</span></span> | <span data-ttu-id="0a45d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0a45d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a45d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a45d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0a45d-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a45d-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a45d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a45d-121">Library</span></span><br/> | <dl> <span data-ttu-id="0a45d-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a45d-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a45d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a45d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a45d-124">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="0a45d-124">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
