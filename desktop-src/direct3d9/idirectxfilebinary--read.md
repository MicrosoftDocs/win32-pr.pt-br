---
description: Lê os dados binários. Preterido.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'Método IDirectXFileBinary:: Read (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012144"
---
# <a name="idirectxfilebinaryread-method"></a><span data-ttu-id="19ed0-104">Método IDirectXFileBinary:: Read</span><span class="sxs-lookup"><span data-stu-id="19ed0-104">IDirectXFileBinary::Read method</span></span>

<span data-ttu-id="19ed0-105">Lê os dados binários.</span><span class="sxs-lookup"><span data-stu-id="19ed0-105">Reads the binary data.</span></span> <span data-ttu-id="19ed0-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="19ed0-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ed0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19ed0-107">Syntax</span></span>


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="19ed0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19ed0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ed0-109">*pvData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="19ed0-109">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ed0-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19ed0-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19ed0-111">Ponteiro para o buffer que recebe os dados que foram lidos.</span><span class="sxs-lookup"><span data-stu-id="19ed0-111">Pointer to the buffer that receives the data that has been read.</span></span>

</dd> <dt>

<span data-ttu-id="19ed0-112">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19ed0-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ed0-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19ed0-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19ed0-114">Tamanho do buffer apontado por pvData, em bytes.</span><span class="sxs-lookup"><span data-stu-id="19ed0-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="19ed0-115">*pcbRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="19ed0-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ed0-116">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19ed0-116">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19ed0-117">Ponteiro para o número de bytes realmente lidos.</span><span class="sxs-lookup"><span data-stu-id="19ed0-117">Pointer to the number of bytes actually read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ed0-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19ed0-118">Return value</span></span>

<span data-ttu-id="19ed0-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19ed0-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19ed0-120">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19ed0-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="19ed0-121">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREDATA.</span><span class="sxs-lookup"><span data-stu-id="19ed0-121">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ed0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ed0-122">Requirements</span></span>



| <span data-ttu-id="19ed0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ed0-123">Requirement</span></span> | <span data-ttu-id="19ed0-124">Valor</span><span class="sxs-lookup"><span data-stu-id="19ed0-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19ed0-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19ed0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="19ed0-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ed0-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="19ed0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19ed0-127">Library</span></span><br/> | <dl> <span data-ttu-id="19ed0-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19ed0-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ed0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="19ed0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ed0-130">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="19ed0-130">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
