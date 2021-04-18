---
description: Recupera os dados para um dos membros do objeto ou os dados de todos os membros. Preterido.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'Método IDirectXFileData:: GetData (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811721"
---
# <a name="idirectxfiledatagetdata-method"></a><span data-ttu-id="0c907-104">Método IDirectXFileData:: GetData</span><span class="sxs-lookup"><span data-stu-id="0c907-104">IDirectXFileData::GetData method</span></span>

<span data-ttu-id="0c907-105">Recupera os dados para um dos membros do objeto ou os dados de todos os membros.</span><span class="sxs-lookup"><span data-stu-id="0c907-105">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="0c907-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="0c907-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c907-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c907-107">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a><span data-ttu-id="0c907-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c907-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c907-109">*szMember* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0c907-109">*szMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c907-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c907-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c907-111">Ponteiro para o nome do membro para o qual recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="0c907-111">Pointer to the name of the member for which to retrieve data.</span></span> <span data-ttu-id="0c907-112">Especifique **NULL** para recuperar todos os dados dos membros necessários.</span><span class="sxs-lookup"><span data-stu-id="0c907-112">Specify **NULL** to retrieve all required members' data.</span></span>

</dd> <dt>

<span data-ttu-id="0c907-113">*pcbSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c907-113">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c907-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c907-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0c907-115">Ponteiro para receber o tamanho do buffer ppvData, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0c907-115">Pointer to receive the ppvData buffer size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0c907-116">*ppvData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c907-116">*ppvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c907-117">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="0c907-117">Type: **void\*\***</span></span>

<span data-ttu-id="0c907-118">Endereço de um ponteiro para o buffer para receber os dados associados a szMember.</span><span class="sxs-lookup"><span data-stu-id="0c907-118">Address of a pointer to the buffer to receive the data associated with szMember.</span></span> <span data-ttu-id="0c907-119">Se szMember for **NULL**, ppvData será definido para apontar para um buffer que contém todos os dados dos membros necessários em um bloco contíguo de memória.</span><span class="sxs-lookup"><span data-stu-id="0c907-119">If szMember is **NULL**, ppvData is set to point to a buffer containing all required members' data in a contiguous block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c907-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c907-120">Return value</span></span>

<span data-ttu-id="0c907-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c907-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c907-122">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c907-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="0c907-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDATAREFERENCE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="0c907-123">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADDataReference, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c907-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c907-124">Remarks</span></span>

<span data-ttu-id="0c907-125">Esse método recupera os dados para os membros necessários de um objeto de dados, mas não dados para Membros (filho) opcionais.</span><span class="sxs-lookup"><span data-stu-id="0c907-125">This method retrieves the data for required members of a data object but no data for optional (child) members.</span></span> <span data-ttu-id="0c907-126">Use [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) para recuperar objetos filho.</span><span class="sxs-lookup"><span data-stu-id="0c907-126">Use [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) to retrieve child objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c907-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c907-127">Requirements</span></span>



| <span data-ttu-id="0c907-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c907-128">Requirement</span></span> | <span data-ttu-id="0c907-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0c907-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c907-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c907-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0c907-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c907-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c907-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c907-132">Library</span></span><br/> | <dl> <span data-ttu-id="0c907-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c907-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c907-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c907-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c907-135">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="0c907-135">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="0c907-136">**IDirectXFileData:: GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="0c907-136">**IDirectXFileData::GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
