---
description: Função de proxy para o método GetChannelCount.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: Função IWICPixelFormatInfo_GetChannelCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761159"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a><span data-ttu-id="10693-103">\_Função de \_ proxy IWICPixelFormatInfo GetChannelCount</span><span class="sxs-lookup"><span data-stu-id="10693-103">IWICPixelFormatInfo\_GetChannelCount\_Proxy function</span></span>

<span data-ttu-id="10693-104">Função de proxy para o método [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) .</span><span class="sxs-lookup"><span data-stu-id="10693-104">Proxy function for the [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="10693-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10693-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a><span data-ttu-id="10693-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10693-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10693-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="10693-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10693-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="10693-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="10693-109">Ponteiro para este objeto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="10693-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="10693-110">*puiChannelCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10693-110">*puiChannelCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10693-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="10693-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="10693-112">Ponteiro que recebe a contagem de canais.</span><span class="sxs-lookup"><span data-stu-id="10693-112">Pointer that receives the channel count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10693-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10693-113">Return value</span></span>

<span data-ttu-id="10693-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="10693-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="10693-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="10693-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="10693-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10693-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="10693-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="10693-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="10693-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10693-118">Requirements</span></span>



| <span data-ttu-id="10693-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10693-119">Requirement</span></span> | <span data-ttu-id="10693-120">Valor</span><span class="sxs-lookup"><span data-stu-id="10693-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10693-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10693-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10693-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10693-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="10693-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10693-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10693-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10693-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="10693-125">DLL</span><span class="sxs-lookup"><span data-stu-id="10693-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10693-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10693-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




