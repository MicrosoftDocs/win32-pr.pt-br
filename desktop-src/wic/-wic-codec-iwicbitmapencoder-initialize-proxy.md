---
description: Função IWICBitmapEncoder_Initialize_Proxy function-proxy para o método Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: Função IWICBitmapEncoder_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d346d1379ae92f19a530c65daff07cb98b2e0e50
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100614"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="ff8ac-103">A \_ função de proxy IWICBitmapEncoder Initialize \_</span><span class="sxs-lookup"><span data-stu-id="ff8ac-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="ff8ac-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) .</span><span class="sxs-lookup"><span data-stu-id="ff8ac-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff8ac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff8ac-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="ff8ac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff8ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff8ac-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="ff8ac-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff8ac-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="ff8ac-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="ff8ac-109">Ponteiro para este objeto [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="ff8ac-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="ff8ac-110">*pIStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff8ac-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff8ac-111">Tipo: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span><span class="sxs-lookup"><span data-stu-id="ff8ac-111">Type: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span></span>

<span data-ttu-id="ff8ac-112">O fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="ff8ac-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="ff8ac-113">*cacheOption* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff8ac-113">*cacheOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff8ac-114">Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="ff8ac-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="ff8ac-115">O [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) usado na inicialização.</span><span class="sxs-lookup"><span data-stu-id="ff8ac-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff8ac-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ff8ac-116">Return value</span></span>

<span data-ttu-id="ff8ac-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff8ac-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ff8ac-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff8ac-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff8ac-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff8ac-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff8ac-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff8ac-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ff8ac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff8ac-121">Requirements</span></span>



| <span data-ttu-id="ff8ac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff8ac-122">Requirement</span></span> | <span data-ttu-id="ff8ac-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ff8ac-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff8ac-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff8ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ff8ac-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff8ac-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ff8ac-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff8ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ff8ac-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff8ac-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ff8ac-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ff8ac-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff8ac-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff8ac-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

