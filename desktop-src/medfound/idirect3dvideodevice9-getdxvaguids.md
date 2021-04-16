---
description: Obtém uma lista de perfis de monitoração de vídeo do DirectX (DXVA) que têm suporte do driver de vídeo.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'Método IDirect3DVideoDevice9:: GetDXVAGuids (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765052"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a><span data-ttu-id="9c805-103">Método IDirect3DVideoDevice9:: GetDXVAGuids</span><span class="sxs-lookup"><span data-stu-id="9c805-103">IDirect3DVideoDevice9::GetDXVAGuids method</span></span>

<span data-ttu-id="9c805-104">Obtém uma lista de perfis de monitoração de vídeo do DirectX (DXVA) que têm suporte do driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c805-104">Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c805-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c805-105">Syntax</span></span>


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a><span data-ttu-id="9c805-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c805-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c805-107">*pNumGuids*</span><span class="sxs-lookup"><span data-stu-id="9c805-107">*pNumGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="9c805-108">Na entrada, especifica o número de elementos na matriz *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="9c805-108">On input, specifies the number of elements in the *pGuids* array.</span></span> <span data-ttu-id="9c805-109">Se *pGuids* for **NULL**, o valor de `*pNumGuids` deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="9c805-109">If *pGuids* is **NULL**, the value of `*pNumGuids` must be zero.</span></span>

<span data-ttu-id="9c805-110">Na saída, se *pGuids* for **NULL**, *pNumGuids* receberá o número de perfis de DXVA de modo restrito.</span><span class="sxs-lookup"><span data-stu-id="9c805-110">On output, if *pGuids* is **NULL**, *pNumGuids* receives the number of restricted-mode DXVA profiles.</span></span> <span data-ttu-id="9c805-111">Caso contrário, *pNumGuids* receberá o número real de GUIDs que são copiados para a matriz *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="9c805-111">Otherwise, *pNumGuids* receives the actual number of GUIDs that are copied to the *pGuids* array.</span></span>

</dd> <dt>

<span data-ttu-id="9c805-112">*pGuids*</span><span class="sxs-lookup"><span data-stu-id="9c805-112">*pGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="9c805-113">Endereço de uma matriz de GUIDs ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9c805-113">Address of an array of GUIDs or **NULL**.</span></span> <span data-ttu-id="9c805-114">Se o valor for não **nulo**, a matriz receberá uma lista de GUIDs que especificam perfis de DXVA de modo restrito.</span><span class="sxs-lookup"><span data-stu-id="9c805-114">If the value is non-**NULL**, the array receives a list of GUIDs that specify restricted-mode DXVA profiles.</span></span> <span data-ttu-id="9c805-115">Esses GUIDs são definidos em DXVA. h e estão documentados na [especificação dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="9c805-115">These GUIDs are defined in dxva.h, and are documented in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c805-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c805-116">Return value</span></span>

<span data-ttu-id="9c805-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9c805-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9c805-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9c805-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c805-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c805-119">Remarks</span></span>

<span data-ttu-id="9c805-120">Chame esse método duas vezes.</span><span class="sxs-lookup"><span data-stu-id="9c805-120">Call this method twice.</span></span> <span data-ttu-id="9c805-121">Na primeira chamada, defina *pGuids* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9c805-121">On the first call, set *pGuids* to **NULL**.</span></span> <span data-ttu-id="9c805-122">O parâmetro *pNumGuids* recebe o número de GUIDs de perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c805-122">The *pNumGuids* parameter receives the number of DXVA profile GUIDs.</span></span> <span data-ttu-id="9c805-123">Aloque uma matriz de GUIDs com o tamanho necessário e chame o método novamente.</span><span class="sxs-lookup"><span data-stu-id="9c805-123">Allocate an array of GUIDs with the required size and call the method again.</span></span> <span data-ttu-id="9c805-124">Desta vez, defina *pGuids* como o endereço da matriz.</span><span class="sxs-lookup"><span data-stu-id="9c805-124">This time, set *pGuids* to the address of the array.</span></span> <span data-ttu-id="9c805-125">O método preenche a matriz com a lista de GUIDs de perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c805-125">The method fills the array with the list of DXVA profile GUIDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c805-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c805-126">Requirements</span></span>



| <span data-ttu-id="9c805-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c805-127">Requirement</span></span> | <span data-ttu-id="9c805-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9c805-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9c805-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c805-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9c805-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c805-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c805-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c805-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9c805-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c805-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c805-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c805-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c805-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c805-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c805-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c805-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c805-136">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="9c805-136">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
