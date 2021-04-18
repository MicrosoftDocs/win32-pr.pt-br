---
description: Função de proxy para o método DoesSupportAnimation.
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: Função IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 443a8ec7871af6161de2efbb6d4f21d65e5ae9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787680"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a><span data-ttu-id="21aa5-103">\_Função de \_ proxy IWICBitmapCodecInfo DoesSupportAnimation</span><span class="sxs-lookup"><span data-stu-id="21aa5-103">IWICBitmapCodecInfo\_DoesSupportAnimation\_Proxy function</span></span>

<span data-ttu-id="21aa5-104">Função de proxy para o método [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) .</span><span class="sxs-lookup"><span data-stu-id="21aa5-104">Proxy function for the [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="21aa5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21aa5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a><span data-ttu-id="21aa5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21aa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21aa5-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="21aa5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21aa5-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="21aa5-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="21aa5-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="21aa5-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="21aa5-110">*pfSupportAnimation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="21aa5-110">*pfSupportAnimation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21aa5-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="21aa5-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="21aa5-112">Um ponteiro que recebe _ *true*\* se o codec dá suporte a imagens com informações de tempo; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="21aa5-112">A pointer that receives _ *TRUE*\* if the codec supports images with timing information; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21aa5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21aa5-113">Return value</span></span>

<span data-ttu-id="21aa5-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="21aa5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="21aa5-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="21aa5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21aa5-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21aa5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21aa5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="21aa5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="21aa5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21aa5-118">Requirements</span></span>



| <span data-ttu-id="21aa5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="21aa5-119">Requirement</span></span> | <span data-ttu-id="21aa5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="21aa5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21aa5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21aa5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21aa5-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21aa5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="21aa5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21aa5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21aa5-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21aa5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="21aa5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="21aa5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21aa5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21aa5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




