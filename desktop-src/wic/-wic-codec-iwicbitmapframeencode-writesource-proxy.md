---
description: Função de proxy para o método WriteState.
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: Função IWICBitmapFrameEncode_WriteSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9eb5ab9db9341d138c72d350304407966a6293d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172191"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a><span data-ttu-id="9b988-103">Função de proxy de \_ gravação de IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="9b988-103">IWICBitmapFrameEncode\_WriteSource\_Proxy function</span></span>

<span data-ttu-id="9b988-104">Função de proxy para o método [**WriteState**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="9b988-104">Proxy function for the [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b988-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b988-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a><span data-ttu-id="9b988-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b988-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b988-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="9b988-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b988-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="9b988-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="9b988-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="9b988-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="9b988-110">*pIBitmapSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b988-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b988-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="9b988-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="9b988-112">A origem do bitmap a ser codificada.</span><span class="sxs-lookup"><span data-stu-id="9b988-112">The bitmap source to encode.</span></span>

</dd> <dt>

<span data-ttu-id="9b988-113">_prc \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b988-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b988-114">Tipo: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="9b988-114">Type: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="9b988-115">O tamanho do retângulo da origem do bitmap.</span><span class="sxs-lookup"><span data-stu-id="9b988-115">The size rectangle of the bitmap source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b988-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b988-116">Return value</span></span>

<span data-ttu-id="9b988-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9b988-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9b988-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9b988-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b988-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b988-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b988-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b988-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9b988-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b988-121">Requirements</span></span>



| <span data-ttu-id="9b988-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b988-122">Requirement</span></span> | <span data-ttu-id="9b988-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9b988-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b988-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b988-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9b988-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b988-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9b988-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b988-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9b988-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b988-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9b988-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9b988-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b988-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b988-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




