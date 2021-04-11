---
description: Cria um dispositivo de decodificador DXVA (DirectX Video Acceleration).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'Método IDirect3DVideoDevice9:: CreateDXVADevice (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090967"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a><span data-ttu-id="9ce83-103">Método IDirect3DVideoDevice9:: CreateDXVADevice</span><span class="sxs-lookup"><span data-stu-id="9ce83-103">IDirect3DVideoDevice9::CreateDXVADevice method</span></span>

<span data-ttu-id="9ce83-104">Cria um dispositivo de decodificador DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="9ce83-104">Creates a DirectX Video Acceleration (DXVA) decoder device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce83-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ce83-105">Syntax</span></span>


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a><span data-ttu-id="9ce83-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ce83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce83-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="9ce83-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce83-108">Ponteiro para um GUID que especifica o dispositivo a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9ce83-108">Pointer to a GUID that specifies the device to create.</span></span>

</dd> <dt>

<span data-ttu-id="9ce83-109">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="9ce83-109">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce83-110">Ponteiro para uma estrutura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica o formato da imagem descompactada.</span><span class="sxs-lookup"><span data-stu-id="9ce83-110">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the format of the uncompressed image.</span></span>

</dd> <dt>

<span data-ttu-id="9ce83-111">*pData*</span><span class="sxs-lookup"><span data-stu-id="9ce83-111">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce83-112">Ponteiro para uma estrutura **DXVA \_ ConnectMode** que especifica o modo DXVA e o perfil restrito.</span><span class="sxs-lookup"><span data-stu-id="9ce83-112">Pointer to a **DXVA\_ConnectMode** structure that specifies the DXVA mode and restricted profile.</span></span>

</dd> <dt>

<span data-ttu-id="9ce83-113">*DataSize*</span><span class="sxs-lookup"><span data-stu-id="9ce83-113">*DataSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce83-114">Tamanho da estrutura **DXVA \_ ConnectMode** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="9ce83-114">Size of the **DXVA\_ConnectMode** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9ce83-115">*ppDXVADevice*</span><span class="sxs-lookup"><span data-stu-id="9ce83-115">*ppDXVADevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce83-116">Recebe um ponteiro para a interface [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) .</span><span class="sxs-lookup"><span data-stu-id="9ce83-116">Receives a pointer to the [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) interface.</span></span> <span data-ttu-id="9ce83-117">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="9ce83-117">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ce83-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ce83-118">Return value</span></span>

<span data-ttu-id="9ce83-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ce83-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ce83-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ce83-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce83-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ce83-121">Requirements</span></span>



| <span data-ttu-id="9ce83-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ce83-122">Requirement</span></span> | <span data-ttu-id="9ce83-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9ce83-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9ce83-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ce83-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce83-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ce83-125">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ce83-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ce83-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce83-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ce83-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9ce83-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ce83-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ce83-129"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce83-129"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce83-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ce83-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce83-131">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="9ce83-131">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




