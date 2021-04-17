---
description: Função de proxy para o método GetPreview.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: Função IWICBitmapDecoder_GetPreview_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790461"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a><span data-ttu-id="06b1f-103">\_Função de proxy IWICBitmapDecoder SetPreview \_</span><span class="sxs-lookup"><span data-stu-id="06b1f-103">IWICBitmapDecoder\_GetPreview\_Proxy function</span></span>

<span data-ttu-id="06b1f-104">Função de proxy para o método [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="06b1f-104">Proxy function for the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06b1f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a><span data-ttu-id="06b1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06b1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b1f-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="06b1f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b1f-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="06b1f-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="06b1f-109">Ponteiro para este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="06b1f-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="06b1f-110">*ppIBitmapSource* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="06b1f-110">*ppIBitmapSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06b1f-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="06b1f-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="06b1f-112">Um ponteiro que recebe um ponteiro para o bitmap de visualização, se houver suporte.</span><span class="sxs-lookup"><span data-stu-id="06b1f-112">A pointer that receives a pointer to the preview bitmap if supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b1f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06b1f-113">Return value</span></span>

<span data-ttu-id="06b1f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06b1f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="06b1f-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="06b1f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06b1f-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06b1f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06b1f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="06b1f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="06b1f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06b1f-118">Requirements</span></span>



| <span data-ttu-id="06b1f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b1f-119">Requirement</span></span> | <span data-ttu-id="06b1f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="06b1f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b1f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06b1f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="06b1f-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06b1f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="06b1f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06b1f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="06b1f-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06b1f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="06b1f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="06b1f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06b1f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06b1f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




