---
description: Função de proxy de função IWICBitmapFrameDecode_GetColorContexts_Proxy para o método GetColorContexts.
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
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100574"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="dedd3-103">\_Função de \_ proxy GetColorContexts IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="dedd3-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="dedd3-104">Função de proxy para o método [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="dedd3-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dedd3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dedd3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="dedd3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dedd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dedd3-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dedd3-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="dedd3-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="dedd3-109">Ponteiro para este objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="dedd3-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="dedd3-110">*conta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dedd3-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="dedd3-111">Type: **UINT**</span></span>

<span data-ttu-id="dedd3-112">O número de contextos de cor a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="dedd3-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="dedd3-113">Esse valor deve ser o tamanho ou menor que o tamanho disponível para *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="dedd3-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="dedd3-114">*ppIColorContexts* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dedd3-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="dedd3-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="dedd3-116">Um ponteiro que recebe um ponteiro para os objetos [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) .</span><span class="sxs-lookup"><span data-stu-id="dedd3-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="dedd3-117">*pcActualCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dedd3-118">Tipo: **uint \***</span><span class="sxs-lookup"><span data-stu-id="dedd3-118">Type: **UINT\***</span></span>

<span data-ttu-id="dedd3-119">Um ponteiro que recebe o número de contextos de cor contidos no quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="dedd3-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dedd3-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dedd3-120">Return value</span></span>

<span data-ttu-id="dedd3-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dedd3-121">Type: **HRESULT**</span></span>

<span data-ttu-id="dedd3-122">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd3-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dedd3-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dedd3-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dedd3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="dedd3-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dedd3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dedd3-125">Requirements</span></span>



| <span data-ttu-id="dedd3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dedd3-126">Requirement</span></span> | <span data-ttu-id="dedd3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="dedd3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dedd3-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dedd3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dedd3-129">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dedd3-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dedd3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dedd3-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dedd3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dedd3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dedd3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dedd3-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dedd3-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




