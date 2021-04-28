---
description: Função IWICBitmapFrameEncode_Commit_Proxy function-proxy para o método Commit.
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
ms.openlocfilehash: 0f8ab87860c77cf58f73491a1fb5fc1b658ed67f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091114"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="4cf09-103">Função de proxy de \_ confirmação de IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="4cf09-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="4cf09-104">Função de proxy para o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .</span><span class="sxs-lookup"><span data-stu-id="4cf09-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf09-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cf09-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="4cf09-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cf09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf09-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="4cf09-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf09-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="4cf09-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="4cf09-109">Ponteiro para este objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="4cf09-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf09-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4cf09-110">Return value</span></span>

<span data-ttu-id="4cf09-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4cf09-111">Type: **HRESULT**</span></span>

<span data-ttu-id="4cf09-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4cf09-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4cf09-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4cf09-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cf09-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cf09-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf09-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cf09-115">Requirements</span></span>



| <span data-ttu-id="4cf09-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cf09-116">Requirement</span></span> | <span data-ttu-id="4cf09-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4cf09-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf09-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cf09-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf09-119">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cf09-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4cf09-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cf09-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf09-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cf09-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4cf09-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf09-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf09-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cf09-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




