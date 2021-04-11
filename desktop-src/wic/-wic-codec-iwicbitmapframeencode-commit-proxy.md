---
description: Função de proxy para o método Commit.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: Função IWICBitmapFrameEncode_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296290"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="e152b-103">Função de proxy de \_ confirmação de IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="e152b-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="e152b-104">Função de proxy para o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .</span><span class="sxs-lookup"><span data-stu-id="e152b-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e152b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e152b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="e152b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e152b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e152b-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="e152b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e152b-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="e152b-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="e152b-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="e152b-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e152b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e152b-110">Return value</span></span>

<span data-ttu-id="e152b-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e152b-111">Type: **HRESULT**</span></span>

<span data-ttu-id="e152b-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e152b-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e152b-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e152b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e152b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e152b-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e152b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e152b-115">Requirements</span></span>



| <span data-ttu-id="e152b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e152b-116">Requirement</span></span> | <span data-ttu-id="e152b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e152b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e152b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e152b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e152b-119">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e152b-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e152b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e152b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e152b-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e152b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e152b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e152b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e152b-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e152b-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




