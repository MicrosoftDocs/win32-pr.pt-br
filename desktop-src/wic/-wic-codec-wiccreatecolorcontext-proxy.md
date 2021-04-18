---
description: Função de proxy para criar um IWICColorContext.
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: Função WICCreateColorContext_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e4861bb1ccb275edc38163335e0da5d26441a334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789236"
---
# <a name="wiccreatecolorcontext_proxy-function"></a><span data-ttu-id="0c390-103">\_Função de proxy WICCreateColorContext</span><span class="sxs-lookup"><span data-stu-id="0c390-103">WICCreateColorContext\_Proxy function</span></span>

<span data-ttu-id="0c390-104">Função de proxy para criar um [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="0c390-104">Proxy function for creating an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c390-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c390-105">Syntax</span></span>


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="0c390-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c390-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c390-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="0c390-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c390-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="0c390-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

<span data-ttu-id="0c390-109">Ponteiro para este objeto [_ *IWICImagingFactory* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) .</span><span class="sxs-lookup"><span data-stu-id="0c390-109">Pointer to this [_ *IWICImagingFactory*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="0c390-110">*ppIColorContext*</span><span class="sxs-lookup"><span data-stu-id="0c390-110">*ppIColorContext*</span></span> 
</dt> <dd>

<span data-ttu-id="0c390-111">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span><span class="sxs-lookup"><span data-stu-id="0c390-111">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c390-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c390-112">Return value</span></span>

<span data-ttu-id="0c390-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0c390-113">Type: **HRESULT**</span></span>

<span data-ttu-id="0c390-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c390-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c390-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c390-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c390-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c390-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0c390-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c390-117">Requirements</span></span>



| <span data-ttu-id="0c390-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c390-118">Requirement</span></span> | <span data-ttu-id="0c390-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0c390-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c390-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c390-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0c390-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c390-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0c390-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c390-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0c390-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c390-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0c390-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0c390-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c390-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c390-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




