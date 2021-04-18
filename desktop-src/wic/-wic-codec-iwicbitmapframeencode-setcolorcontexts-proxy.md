---
description: Função de proxy para o método SetColorContexts.
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: Função IWICBitmapFrameEncode_SetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8a960873340c15772113a3f1553a9b6e16c44338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789341"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a><span data-ttu-id="9aa2d-103">\_Função de proxy SetColorContexts de IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="9aa2d-103">IWICBitmapFrameEncode\_SetColorContexts\_Proxy function</span></span>

<span data-ttu-id="9aa2d-104">Função de proxy para o método [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="9aa2d-104">Proxy function for the [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa2d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aa2d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="9aa2d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aa2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa2d-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="9aa2d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa2d-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="9aa2d-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="9aa2d-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="9aa2d-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="9aa2d-110">*conta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aa2d-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa2d-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9aa2d-111">Type: **UINT**</span></span>

<span data-ttu-id="9aa2d-112">O número de perfis de [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="9aa2d-112">The number of [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) profiles to set.</span></span>

</dd> <dt>

<span data-ttu-id="9aa2d-113">*ppIColorContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aa2d-113">*ppIColorContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa2d-114">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="9aa2d-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="9aa2d-115">Um ponteiro para um ponteiro [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) que contém os perfis de contextos de cor a serem definidos para o quadro.</span><span class="sxs-lookup"><span data-stu-id="9aa2d-115">A pointer to an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) pointer containing the color contexts profiles to set to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa2d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9aa2d-116">Return value</span></span>

<span data-ttu-id="9aa2d-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9aa2d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="9aa2d-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9aa2d-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9aa2d-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9aa2d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa2d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aa2d-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa2d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa2d-121">Requirements</span></span>



| <span data-ttu-id="9aa2d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa2d-122">Requirement</span></span> | <span data-ttu-id="9aa2d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa2d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa2d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa2d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa2d-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9aa2d-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9aa2d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa2d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa2d-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9aa2d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9aa2d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9aa2d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aa2d-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aa2d-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




