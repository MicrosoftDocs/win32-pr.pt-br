---
description: Função de proxy para o método GetDecoderInfo.
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: Função IWICBitmapDecoder_GetDecoderInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461072"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a><span data-ttu-id="6e950-103">\_Função de \_ proxy IWICBitmapDecoder GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="6e950-103">IWICBitmapDecoder\_GetDecoderInfo\_Proxy function</span></span>

<span data-ttu-id="6e950-104">Função de proxy para o método [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="6e950-104">Proxy function for the [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e950-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e950-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6e950-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e950-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6e950-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e950-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6e950-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="6e950-109">Ponteiro para este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="6e950-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="6e950-110">*ppIDecoderInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e950-110">*ppIDecoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e950-111">Tipo: **[ **IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="6e950-111">Type: **[**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span></span>

<span data-ttu-id="6e950-112">Um ponteiro que recebe um ponteiro para um [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span><span class="sxs-lookup"><span data-stu-id="6e950-112">A pointer that receives a pointer to an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e950-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e950-113">Return value</span></span>

<span data-ttu-id="6e950-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6e950-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6e950-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e950-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e950-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e950-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e950-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e950-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6e950-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e950-118">Requirements</span></span>



| <span data-ttu-id="6e950-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e950-119">Requirement</span></span> | <span data-ttu-id="6e950-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6e950-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e950-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e950-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e950-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e950-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6e950-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e950-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e950-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e950-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6e950-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e950-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e950-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e950-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




