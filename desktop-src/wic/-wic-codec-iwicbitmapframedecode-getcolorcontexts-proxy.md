---
description: Função de proxy para o método GetColorContexts.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: Função IWICBitmapFrameDecode_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e22166e98e4ef276a6bf1d72dfc860cf8fb511e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164423"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="3b5c4-103">\_Função de \_ proxy GetColorContexts IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="3b5c4-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="3b5c4-104">Função de proxy para o método [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="3b5c4-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b5c4-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="3b5c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b5c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b5c4-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="3b5c4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b5c4-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="3b5c4-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="3b5c4-109">Ponteiro para este objeto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="3b5c4-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="3b5c4-110">*conta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b5c4-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b5c4-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3b5c4-111">Type: **UINT**</span></span>

<span data-ttu-id="3b5c4-112">O número de contextos de cor a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="3b5c4-113">Esse valor deve ser o tamanho ou menor que o tamanho disponível para *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="3b5c4-114">*ppIColorContexts* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3b5c4-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b5c4-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="3b5c4-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="3b5c4-116">Um ponteiro que recebe um ponteiro para os objetos [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) .</span><span class="sxs-lookup"><span data-stu-id="3b5c4-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="3b5c4-117">*pcActualCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3b5c4-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b5c4-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="3b5c4-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="3b5c4-119">Um ponteiro que recebe o número de contextos de cor contidos no quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b5c4-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b5c4-120">Return value</span></span>

<span data-ttu-id="3b5c4-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3b5c4-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3b5c4-122">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b5c4-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b5c4-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b5c4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b5c4-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5c4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b5c4-125">Requirements</span></span>



| <span data-ttu-id="3b5c4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5c4-126">Requirement</span></span> | <span data-ttu-id="3b5c4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3b5c4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5c4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b5c4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5c4-129">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b5c4-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3b5c4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b5c4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5c4-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b5c4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3b5c4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3b5c4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b5c4-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b5c4-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




