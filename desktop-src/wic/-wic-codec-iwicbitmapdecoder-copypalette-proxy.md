---
description: Função de proxy para o método CopyPalette.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: Função IWICBitmapDecoder_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6902668a9c4feffdcc696ce0d5f6214a707bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786254"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="96d14-103">\_Função de \_ proxy IWICBitmapDecoder CopyPalette</span><span class="sxs-lookup"><span data-stu-id="96d14-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="96d14-104">Função de proxy para o método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="96d14-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d14-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96d14-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="96d14-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96d14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d14-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="96d14-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d14-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="96d14-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="96d14-109">Ponteiro para este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="96d14-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="96d14-110">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96d14-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d14-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="96d14-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="96d14-112">A paleta de imagens a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="96d14-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d14-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96d14-113">Return value</span></span>

<span data-ttu-id="96d14-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="96d14-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="96d14-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96d14-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96d14-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96d14-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d14-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="96d14-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="96d14-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96d14-118">Requirements</span></span>



| <span data-ttu-id="96d14-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d14-119">Requirement</span></span> | <span data-ttu-id="96d14-120">Valor</span><span class="sxs-lookup"><span data-stu-id="96d14-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d14-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96d14-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96d14-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96d14-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="96d14-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96d14-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96d14-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96d14-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="96d14-125">DLL</span><span class="sxs-lookup"><span data-stu-id="96d14-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96d14-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96d14-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




