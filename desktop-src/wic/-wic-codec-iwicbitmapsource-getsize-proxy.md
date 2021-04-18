---
description: Função de proxy para o método GetSize.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: Função IWICBitmapSource_GetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760684"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a><span data-ttu-id="e5dd7-103">\_Função de \_ proxy IWICBitmapSource GetSize</span><span class="sxs-lookup"><span data-stu-id="e5dd7-103">IWICBitmapSource\_GetSize\_Proxy function</span></span>

<span data-ttu-id="e5dd7-104">Função de proxy para o método [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .</span><span class="sxs-lookup"><span data-stu-id="e5dd7-104">Proxy function for the [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5dd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5dd7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="e5dd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5dd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5dd7-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="e5dd7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dd7-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="e5dd7-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="e5dd7-109">Ponteiro para este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="e5dd7-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="e5dd7-110">*puiWidth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e5dd7-110">*puiWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dd7-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="e5dd7-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="e5dd7-112">Um ponteiro que recebe a largura de pixel do bitmap.</span><span class="sxs-lookup"><span data-stu-id="e5dd7-112">A pointer that receives the pixel width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e5dd7-113">_puiHeight \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e5dd7-113">_puiHeight\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5dd7-114">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="e5dd7-114">Type: \**UINT\** _</span></span>

<span data-ttu-id="e5dd7-115">Um ponteiro que recebe a altura do pixel do bitmap</span><span class="sxs-lookup"><span data-stu-id="e5dd7-115">A pointer that receives the pixel height of the bitmap</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5dd7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5dd7-116">Return value</span></span>

<span data-ttu-id="e5dd7-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e5dd7-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e5dd7-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e5dd7-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5dd7-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e5dd7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5dd7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5dd7-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e5dd7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5dd7-121">Requirements</span></span>



| <span data-ttu-id="e5dd7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5dd7-122">Requirement</span></span> | <span data-ttu-id="e5dd7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e5dd7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5dd7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5dd7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e5dd7-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5dd7-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e5dd7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5dd7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e5dd7-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5dd7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e5dd7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e5dd7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5dd7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5dd7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




