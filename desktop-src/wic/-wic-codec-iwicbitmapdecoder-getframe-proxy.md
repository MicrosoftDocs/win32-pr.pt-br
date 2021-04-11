---
description: Função de proxy para o método GetFrame.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: Função IWICBitmapDecoder_GetFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296294"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a><span data-ttu-id="b8c49-103">\_Função de proxy de SETFRAME IWICBitmapDecoder \_</span><span class="sxs-lookup"><span data-stu-id="b8c49-103">IWICBitmapDecoder\_GetFrame\_Proxy function</span></span>

<span data-ttu-id="b8c49-104">Função de proxy para o método [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) .</span><span class="sxs-lookup"><span data-stu-id="b8c49-104">Proxy function for the [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c49-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8c49-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a><span data-ttu-id="b8c49-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8c49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8c49-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="b8c49-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8c49-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="b8c49-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="b8c49-109">Ponteiro para este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="b8c49-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="b8c49-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b8c49-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8c49-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b8c49-111">Type: **UINT**</span></span>

<span data-ttu-id="b8c49-112">O quadro específico a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="b8c49-112">The particular frame to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b8c49-113">*ppIBitmapFrame* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b8c49-113">*ppIBitmapFrame* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8c49-114">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8c49-114">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span></span>

<span data-ttu-id="b8c49-115">Um ponteiro que recebe um ponteiro para o [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="b8c49-115">A pointer that receives a pointer to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8c49-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8c49-116">Return value</span></span>

<span data-ttu-id="b8c49-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b8c49-117">Type: **HRESULT**</span></span>

<span data-ttu-id="b8c49-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b8c49-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8c49-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8c49-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c49-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8c49-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c49-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8c49-121">Requirements</span></span>



| <span data-ttu-id="b8c49-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8c49-122">Requirement</span></span> | <span data-ttu-id="b8c49-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b8c49-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c49-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8c49-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b8c49-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8c49-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b8c49-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8c49-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b8c49-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8c49-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b8c49-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b8c49-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8c49-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8c49-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




