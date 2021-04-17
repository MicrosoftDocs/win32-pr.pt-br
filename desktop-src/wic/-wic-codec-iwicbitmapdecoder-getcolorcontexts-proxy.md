---
description: Função de proxy para o método GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: Função IWICBitmapDecoder_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765275"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="5c7ec-103">\_Função de \_ proxy IWICBitmapDecoder GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="5c7ec-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="5c7ec-104">Função de proxy para o método [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="5c7ec-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c7ec-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="5c7ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c7ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c7ec-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="5c7ec-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="5c7ec-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="5c7ec-109">Ponteiro para este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="5c7ec-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="5c7ec-110">*conta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c7ec-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-111">Type: **UINT**</span></span>

<span data-ttu-id="5c7ec-112">O número de contextos de cor a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="5c7ec-113">Esse valor deve ser o tamanho ou menor que o tamanho disponível para *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="5c7ec-114">*ppIColorContexts* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5c7ec-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c7ec-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="5c7ec-116">Um ponteiro que recebe um ponteiro para o [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="5c7ec-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="5c7ec-117">*pcActualCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c7ec-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="5c7ec-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="5c7ec-119">Um ponteiro que recebe o número de contextos de cor contidos na imagem.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c7ec-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c7ec-120">Return value</span></span>

<span data-ttu-id="5c7ec-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5c7ec-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5c7ec-122">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c7ec-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c7ec-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c7ec-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c7ec-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7ec-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c7ec-125">Requirements</span></span>



| <span data-ttu-id="5c7ec-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7ec-126">Requirement</span></span> | <span data-ttu-id="5c7ec-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5c7ec-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7ec-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7ec-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7ec-129">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c7ec-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5c7ec-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7ec-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7ec-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c7ec-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5c7ec-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5c7ec-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c7ec-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c7ec-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




