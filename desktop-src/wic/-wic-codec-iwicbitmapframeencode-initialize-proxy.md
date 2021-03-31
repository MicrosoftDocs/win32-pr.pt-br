---
description: Função de proxy para o método Initialize.
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: Função IWICBitmapFrameEncode_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: da9192409636de96dbd9d35d9614df2c926c9032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647079"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="600ed-103">Função de proxy de \_ inicialização IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="600ed-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="600ed-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="600ed-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="600ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="600ed-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="600ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="600ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="600ed-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="600ed-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="600ed-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="600ed-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="600ed-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="600ed-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="600ed-110">*pIEncoderOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="600ed-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="600ed-111">Tipo: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="600ed-111">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="600ed-112">O conjunto de propriedades a ser usado para a inicialização [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="600ed-112">The set of properties to use for [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="600ed-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="600ed-113">Return value</span></span>

<span data-ttu-id="600ed-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="600ed-114">Type: **HRESULT**</span></span>

<span data-ttu-id="600ed-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="600ed-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="600ed-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="600ed-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="600ed-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="600ed-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="600ed-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="600ed-118">Requirements</span></span>



| <span data-ttu-id="600ed-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="600ed-119">Requirement</span></span> | <span data-ttu-id="600ed-120">Valor</span><span class="sxs-lookup"><span data-stu-id="600ed-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600ed-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="600ed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="600ed-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="600ed-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="600ed-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="600ed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="600ed-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="600ed-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="600ed-125">DLL</span><span class="sxs-lookup"><span data-stu-id="600ed-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="600ed-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="600ed-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

