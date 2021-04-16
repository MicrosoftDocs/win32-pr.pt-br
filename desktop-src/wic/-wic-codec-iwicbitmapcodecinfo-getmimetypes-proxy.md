---
description: Função de proxy para o método getmimetypes.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: Função IWICBitmapCodecInfo_GetMimeTypes_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501616"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a><span data-ttu-id="37a10-103">\_Função de proxy IWICBitmapCodecInfo Getmimetypes \_</span><span class="sxs-lookup"><span data-stu-id="37a10-103">IWICBitmapCodecInfo\_GetMimeTypes\_Proxy function</span></span>

<span data-ttu-id="37a10-104">Função de proxy para o método [**Getmimetypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .</span><span class="sxs-lookup"><span data-stu-id="37a10-104">Proxy function for the [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37a10-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="37a10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37a10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a10-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="37a10-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a10-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="37a10-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="37a10-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="37a10-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="37a10-110">*cchMimeTypes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37a10-110">*cchMimeTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a10-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="37a10-111">Type: **UINT**</span></span>

<span data-ttu-id="37a10-112">O tamanho do buffer de tipos MIME.</span><span class="sxs-lookup"><span data-stu-id="37a10-112">The size of the mime types buffer.</span></span>

</dd> <dt>

<span data-ttu-id="37a10-113">*wzMimeTypes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="37a10-113">*wzMimeTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37a10-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="37a10-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="37a10-115">Um ponteiro que recebe os tipos MIME associados ao codec.</span><span class="sxs-lookup"><span data-stu-id="37a10-115">A pointer that receives the mime types associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="37a10-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="37a10-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37a10-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="37a10-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="37a10-118">O tamanho real do buffer necessário para recuperar todos os tipos MIME associados ao codec.</span><span class="sxs-lookup"><span data-stu-id="37a10-118">The actual buffer size needed to retrieve all mime types associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37a10-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37a10-119">Return value</span></span>

<span data-ttu-id="37a10-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="37a10-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="37a10-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="37a10-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="37a10-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="37a10-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a10-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="37a10-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="37a10-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37a10-124">Requirements</span></span>



| <span data-ttu-id="37a10-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="37a10-125">Requirement</span></span> | <span data-ttu-id="37a10-126">Valor</span><span class="sxs-lookup"><span data-stu-id="37a10-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a10-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37a10-127">Minimum supported client</span></span><br/> | <span data-ttu-id="37a10-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37a10-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="37a10-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37a10-129">Minimum supported server</span></span><br/> | <span data-ttu-id="37a10-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37a10-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="37a10-131">DLL</span><span class="sxs-lookup"><span data-stu-id="37a10-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37a10-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37a10-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




