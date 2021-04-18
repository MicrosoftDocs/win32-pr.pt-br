---
description: Função de proxy para o método resolution.
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: Função IWICBitmapFrameEncode_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9801384e305f2449c6a31b80cb238fc92f7b63b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810658"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="6752b-103">Função de proxy de resolution de IWICBitmapFrameEncode \_ \_</span><span class="sxs-lookup"><span data-stu-id="6752b-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="6752b-104">Função de proxy para o método [**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="6752b-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6752b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6752b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="6752b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6752b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6752b-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6752b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6752b-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="6752b-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="6752b-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="6752b-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="6752b-110">*DpiX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6752b-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6752b-111">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="6752b-111">Type: **double**</span></span>

<span data-ttu-id="6752b-112">O valor de resolução horizontal.</span><span class="sxs-lookup"><span data-stu-id="6752b-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="6752b-113">*DpiY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6752b-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6752b-114">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="6752b-114">Type: **double**</span></span>

<span data-ttu-id="6752b-115">O valor de resolução vertical.</span><span class="sxs-lookup"><span data-stu-id="6752b-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6752b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6752b-116">Return value</span></span>

<span data-ttu-id="6752b-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6752b-117">Type: **HRESULT**</span></span>

<span data-ttu-id="6752b-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6752b-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6752b-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6752b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6752b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6752b-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6752b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6752b-121">Requirements</span></span>



| <span data-ttu-id="6752b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6752b-122">Requirement</span></span> | <span data-ttu-id="6752b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6752b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6752b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6752b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6752b-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6752b-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6752b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6752b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6752b-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6752b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6752b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6752b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6752b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6752b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




