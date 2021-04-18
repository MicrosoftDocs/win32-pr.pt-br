---
description: Função de proxy para o método GetEncoderInfo.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: Função IWICBitmapEncoder_GetEncoderInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811428"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a><span data-ttu-id="f4934-103">\_Função de \_ proxy IWICBitmapEncoder GetEncoderInfo</span><span class="sxs-lookup"><span data-stu-id="f4934-103">IWICBitmapEncoder\_GetEncoderInfo\_Proxy function</span></span>

<span data-ttu-id="f4934-104">Função de proxy para o método [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="f4934-104">Proxy function for the [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4934-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4934-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f4934-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4934-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4934-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="f4934-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4934-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="f4934-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="f4934-109">Ponteiro para este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="f4934-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="f4934-110">*ppIEncoderInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f4934-110">*ppIEncoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4934-111">Tipo: **[ **IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="f4934-111">Type: **[**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span></span>

<span data-ttu-id="f4934-112">Um ponteiro que recebe um ponteiro para um [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span><span class="sxs-lookup"><span data-stu-id="f4934-112">A pointer that receives a pointer to an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4934-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4934-113">Return value</span></span>

<span data-ttu-id="f4934-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f4934-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f4934-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f4934-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f4934-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4934-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4934-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4934-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f4934-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4934-118">Requirements</span></span>



| <span data-ttu-id="f4934-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4934-119">Requirement</span></span> | <span data-ttu-id="f4934-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f4934-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4934-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4934-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4934-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4934-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f4934-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4934-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4934-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4934-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f4934-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f4934-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4934-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4934-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




