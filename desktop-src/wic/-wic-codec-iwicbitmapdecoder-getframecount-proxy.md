---
description: Função de proxy para o método GetFrameCount.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: Função IWICBitmapDecoder_GetFrameCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647084"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a><span data-ttu-id="c9e19-103">\_Função de \_ proxy IWICBitmapDecoder GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="c9e19-103">IWICBitmapDecoder\_GetFrameCount\_Proxy function</span></span>

<span data-ttu-id="c9e19-104">Função de proxy para o método [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="c9e19-104">Proxy function for the [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9e19-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="c9e19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9e19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9e19-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="c9e19-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e19-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="c9e19-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="c9e19-109">Ponteiro para este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="c9e19-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="c9e19-110">*pCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c9e19-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e19-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="c9e19-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="c9e19-112">Um ponteiro que recebe o número total de quadros na imagem.</span><span class="sxs-lookup"><span data-stu-id="c9e19-112">A pointer that receives the total number of frames in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9e19-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9e19-113">Return value</span></span>

<span data-ttu-id="c9e19-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c9e19-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c9e19-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c9e19-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9e19-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9e19-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9e19-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9e19-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e19-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9e19-118">Requirements</span></span>



| <span data-ttu-id="c9e19-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9e19-119">Requirement</span></span> | <span data-ttu-id="c9e19-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c9e19-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e19-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9e19-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c9e19-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9e19-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c9e19-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9e19-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c9e19-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9e19-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c9e19-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c9e19-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9e19-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9e19-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




