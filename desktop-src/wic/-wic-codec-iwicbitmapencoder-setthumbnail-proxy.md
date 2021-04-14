---
description: Função de proxy para o método SetThumbnail.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: Função IWICBitmapEncoder_SetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d2670dae0d8ba9eeda7ca1d6dce5d3957dc59b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461070"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="6e936-103">\_Função de proxy IWICBitmapEncoder SetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="6e936-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="6e936-104">Função de proxy para o método [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="6e936-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e936-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e936-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="6e936-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e936-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e936-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6e936-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e936-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6e936-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="6e936-109">Ponteiro para este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="6e936-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="6e936-110">*pIThumbnail* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e936-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e936-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="6e936-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="6e936-112">O [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) a ser definido como a miniatura global.</span><span class="sxs-lookup"><span data-stu-id="6e936-112">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e936-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e936-113">Return value</span></span>

<span data-ttu-id="6e936-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6e936-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6e936-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e936-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e936-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e936-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e936-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e936-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6e936-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e936-118">Requirements</span></span>



| <span data-ttu-id="6e936-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e936-119">Requirement</span></span> | <span data-ttu-id="6e936-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6e936-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e936-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e936-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e936-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e936-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6e936-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e936-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e936-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e936-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6e936-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e936-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e936-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e936-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




