---
description: Função de proxy para o método setSize.
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: Função IWICBitmapFrameEncode_SetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790460"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a><span data-ttu-id="33496-103">\_Função de proxy IWICBitmapFrameEncode SetSize \_</span><span class="sxs-lookup"><span data-stu-id="33496-103">IWICBitmapFrameEncode\_SetSize\_Proxy function</span></span>

<span data-ttu-id="33496-104">Função de proxy para o método [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) .</span><span class="sxs-lookup"><span data-stu-id="33496-104">Proxy function for the [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33496-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33496-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="33496-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33496-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33496-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="33496-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33496-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="33496-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="33496-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="33496-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="33496-110">*uiWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33496-110">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33496-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="33496-111">Type: **UINT**</span></span>

<span data-ttu-id="33496-112">A largura da imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="33496-112">The width of the output image.</span></span>

</dd> <dt>

<span data-ttu-id="33496-113">*uiHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33496-113">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33496-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="33496-114">Type: **UINT**</span></span>

<span data-ttu-id="33496-115">A altura da imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="33496-115">The height of the output image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33496-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33496-116">Return value</span></span>

<span data-ttu-id="33496-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="33496-117">Type: **HRESULT**</span></span>

<span data-ttu-id="33496-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33496-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33496-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33496-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33496-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="33496-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="33496-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33496-121">Requirements</span></span>



| <span data-ttu-id="33496-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="33496-122">Requirement</span></span> | <span data-ttu-id="33496-123">Valor</span><span class="sxs-lookup"><span data-stu-id="33496-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33496-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33496-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33496-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33496-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="33496-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33496-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33496-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33496-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="33496-128">DLL</span><span class="sxs-lookup"><span data-stu-id="33496-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33496-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33496-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




