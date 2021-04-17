---
description: Obtém uma lista de formatos de pixel não compactados que podem ser processados usando um perfil de DXVA (DirectX Video Acceleration) especificado.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'Método IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296664"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a><span data-ttu-id="0c478-103">Método IDirect3DVideoDevice9:: GetUncompressedDXVAFormats</span><span class="sxs-lookup"><span data-stu-id="0c478-103">IDirect3DVideoDevice9::GetUncompressedDXVAFormats method</span></span>

<span data-ttu-id="0c478-104">Obtém uma lista de formatos de pixel não compactados que podem ser processados usando um perfil de DXVA (DirectX Video Acceleration) especificado.</span><span class="sxs-lookup"><span data-stu-id="0c478-104">Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c478-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c478-105">Syntax</span></span>


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a><span data-ttu-id="0c478-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c478-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c478-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="0c478-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="0c478-108">Ponteiro para um GUID que especifica o perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="0c478-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="0c478-109">Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="0c478-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c478-110">*pNumFormats*</span><span class="sxs-lookup"><span data-stu-id="0c478-110">*pNumFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="0c478-111">Na entrada, especifica o número de elementos na matriz *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="0c478-111">On input, specifies the number of elements in the *pFormats* array.</span></span> <span data-ttu-id="0c478-112">Se *pFormats* for **NULL**, o valor de `*pNumFormats` deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c478-112">If *pFormats* is **NULL**, the value of `*pNumFormats` must be zero.</span></span>

<span data-ttu-id="0c478-113">Na saída, se *pFormats* for **NULL**, *pNumFormats* receberá o número de formatos de pixel com suporte.</span><span class="sxs-lookup"><span data-stu-id="0c478-113">On output, if *pFormats* is **NULL**, *pNumFormats* receives the number of supported pixel formats.</span></span> <span data-ttu-id="0c478-114">Caso contrário, *pNumFormats* receberá o número real de formatos de pixel copiados para a matriz *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="0c478-114">Otherwise, *pNumFormats* receives the actual number of pixel formats copied to the *pFormats* array.</span></span>

</dd> <dt>

<span data-ttu-id="0c478-115">*pFormats*</span><span class="sxs-lookup"><span data-stu-id="0c478-115">*pFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="0c478-116">Endereço de uma matriz de valores **D3DFORMAT** ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c478-116">Address of an array of **D3DFORMAT** values, or **NULL**.</span></span> <span data-ttu-id="0c478-117">Se o valor for não **nulo**, a matriz receberá uma lista de formatos de pixel.</span><span class="sxs-lookup"><span data-stu-id="0c478-117">If the value is non-**NULL**, the array receives a list of pixel formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c478-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c478-118">Return value</span></span>

<span data-ttu-id="0c478-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c478-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c478-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c478-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c478-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c478-121">Remarks</span></span>

<span data-ttu-id="0c478-122">Chame esse método duas vezes.</span><span class="sxs-lookup"><span data-stu-id="0c478-122">Call this method twice.</span></span> <span data-ttu-id="0c478-123">Na primeira chamada, defina *pFormats* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0c478-123">On the first call, set *pFormats* to **NULL**.</span></span> <span data-ttu-id="0c478-124">O parâmetro *pNumFormats* recebe o número de formatos.</span><span class="sxs-lookup"><span data-stu-id="0c478-124">The *pNumFormats* parameter receives the number of formats.</span></span> <span data-ttu-id="0c478-125">Aloque uma matriz **D3DFORMAT** com o tamanho necessário e chame o método novamente.</span><span class="sxs-lookup"><span data-stu-id="0c478-125">Allocate a **D3DFORMAT** array with the required size, and call the method again.</span></span> <span data-ttu-id="0c478-126">Desta vez, defina *pFormats* como o endereço da matriz.</span><span class="sxs-lookup"><span data-stu-id="0c478-126">This time, set *pFormats* to the address of the array.</span></span> <span data-ttu-id="0c478-127">O método preenche a matriz com a lista de formatos de pixel.</span><span class="sxs-lookup"><span data-stu-id="0c478-127">The method fills the array with the list of pixel formats.</span></span>

<span data-ttu-id="0c478-128">O driver deve retornar os formatos em ordem decrescente de preferência, com o formato mais preferencial listado primeiro.</span><span class="sxs-lookup"><span data-stu-id="0c478-128">The driver should return the formats in decreasing order of preference, with the most preferred format listed first.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c478-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c478-129">Requirements</span></span>



| <span data-ttu-id="0c478-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c478-130">Requirement</span></span> | <span data-ttu-id="0c478-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0c478-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0c478-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c478-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0c478-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c478-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c478-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c478-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0c478-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c478-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0c478-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c478-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c478-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c478-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c478-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c478-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c478-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="0c478-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




