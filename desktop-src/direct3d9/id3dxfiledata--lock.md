---
description: Acessa os dados do arquivo. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'Método ID3DXFileData:: Lock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798525"
---
# <a name="id3dxfiledatalock-method"></a><span data-ttu-id="741ee-103">Método ID3DXFileData:: Lock</span><span class="sxs-lookup"><span data-stu-id="741ee-103">ID3DXFileData::Lock method</span></span>

<span data-ttu-id="741ee-104">Acessa os dados do arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="741ee-104">Accesses the .x file data.</span></span>

## <a name="syntax"></a><span data-ttu-id="741ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="741ee-105">Syntax</span></span>


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="741ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="741ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741ee-107">*psize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="741ee-107">*pSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741ee-108">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="741ee-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="741ee-109">Ponteiro para o tamanho dos dados do arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="741ee-109">Pointer to the size of the .x file data.</span></span>

</dd> <dt>

<span data-ttu-id="741ee-110">*ppData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="741ee-110">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741ee-111">Tipo: **const void \* \***</span><span class="sxs-lookup"><span data-stu-id="741ee-111">Type: **const VOID\*\***</span></span>

<span data-ttu-id="741ee-112">Endereço de um ponteiro para receber o ponteiro de interface do objeto de dados do arquivo [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="741ee-112">Address of a pointer to receive the [**ID3DXFileData**](id3dxfiledata.md) file data object's interface pointer.</span></span> <span data-ttu-id="741ee-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="741ee-113">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741ee-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="741ee-114">Return value</span></span>

<span data-ttu-id="741ee-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="741ee-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="741ee-116">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="741ee-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="741ee-117">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="741ee-117">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="741ee-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="741ee-118">Remarks</span></span>

<span data-ttu-id="741ee-119">O ponteiro *ppData* só é válido durante um **ID3DXFileData:: Lock** ... [**ID3DXFileData:: desbloquear**](id3dxfiledata--unlock.md) sequência.</span><span class="sxs-lookup"><span data-stu-id="741ee-119">The *ppData* pointer is only valid during a **ID3DXFileData::Lock** ... [**ID3DXFileData::Unlock**](id3dxfiledata--unlock.md) sequence.</span></span> <span data-ttu-id="741ee-120">Você pode fazer várias chamadas de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="741ee-120">You can make multiple lock calls.</span></span> <span data-ttu-id="741ee-121">No entanto, você deve garantir que o número de chamadas de bloqueio corresponda ao número de chamadas de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="741ee-121">However, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="741ee-122">Como os dados de arquivo não têm garantia de serem alinhados corretamente com limites de byte, você deve acessar *ppData* com ponteiros não alinhados.</span><span class="sxs-lookup"><span data-stu-id="741ee-122">Because file data is not guaranteed to be aligned properly with byte boundaries, you should access *ppData* with UNALIGNED pointers.</span></span>

<span data-ttu-id="741ee-123">Não há garantia de que os valores de parâmetro retornados sejam válidos devido à possível corrupção de arquivo; Portanto, seu código deve verificar os valores de parâmetro retornados.</span><span class="sxs-lookup"><span data-stu-id="741ee-123">Returned parameter values are not guaranteed to be valid due to possible file corruption; therefore, your code should verify the returned parameter values.</span></span>

## <a name="requirements"></a><span data-ttu-id="741ee-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="741ee-124">Requirements</span></span>



| <span data-ttu-id="741ee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="741ee-125">Requirement</span></span> | <span data-ttu-id="741ee-126">Valor</span><span class="sxs-lookup"><span data-stu-id="741ee-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="741ee-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="741ee-127">Header</span></span><br/>  | <dl> <span data-ttu-id="741ee-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="741ee-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="741ee-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="741ee-129">Library</span></span><br/> | <dl> <span data-ttu-id="741ee-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="741ee-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="741ee-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="741ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741ee-132">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="741ee-132">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
