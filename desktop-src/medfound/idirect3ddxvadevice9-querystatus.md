---
description: Consulta o status de leitura/gravação de uma superfície de decodificação de aceleração de vídeo do DirectX (DXVA).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'Método IDirect3DDXVADevice9:: QueryStatus (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814467"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a><span data-ttu-id="1ff2a-103">Método IDirect3DDXVADevice9:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="1ff2a-103">IDirect3DDXVADevice9::QueryStatus method</span></span>

<span data-ttu-id="1ff2a-104">Consulta o status de leitura/gravação de uma superfície de decodificação de aceleração de vídeo do DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="1ff2a-104">Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ff2a-105">Syntax</span></span>


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="1ff2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ff2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff2a-107">*pSurface*</span><span class="sxs-lookup"><span data-stu-id="1ff2a-107">*pSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff2a-108">Ponteiro para a interface **IDirect3DSurface9** da superfície a ser consultada.</span><span class="sxs-lookup"><span data-stu-id="1ff2a-108">Pointer to the **IDirect3DSurface9** interface of the surface to query.</span></span>

</dd> <dt>

<span data-ttu-id="1ff2a-109">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="1ff2a-109">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff2a-110">Especifica o tipo de consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="1ff2a-110">Specifies the type of query to perform.</span></span>



| <span data-ttu-id="1ff2a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1ff2a-111">Value</span></span>                                                                                                                             | <span data-ttu-id="1ff2a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="1ff2a-112">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <span data-ttu-id="1ff2a-113"><dt>**0x00**</dt></span><span class="sxs-lookup"><span data-stu-id="1ff2a-113"><dt>**0x00**</dt></span></span> </dl> | <span data-ttu-id="1ff2a-114">Teste se a superfície é segura para ser usada para gravação.</span><span class="sxs-lookup"><span data-stu-id="1ff2a-114">Test whether the surface is safe to use for writing.</span></span><br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <span data-ttu-id="1ff2a-115"><dt>**0x01**</dt></span><span class="sxs-lookup"><span data-stu-id="1ff2a-115"><dt>**0x01**</dt></span></span> </dl> | <span data-ttu-id="1ff2a-116">Teste se a superfície é segura para ser usada para leitura.</span><span class="sxs-lookup"><span data-stu-id="1ff2a-116">Test whether the surface is safe to use for reading.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff2a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ff2a-117">Return value</span></span>

<span data-ttu-id="1ff2a-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1ff2a-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ff2a-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ff2a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff2a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ff2a-120">Requirements</span></span>



| <span data-ttu-id="1ff2a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ff2a-121">Requirement</span></span> | <span data-ttu-id="1ff2a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1ff2a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1ff2a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ff2a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff2a-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ff2a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ff2a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ff2a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff2a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ff2a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ff2a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ff2a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff2a-128"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff2a-128"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff2a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ff2a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff2a-130">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="1ff2a-130">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




