---
description: Função de proxy para o método DoesSupportMultiframe.
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: Função IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090279"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a><span data-ttu-id="c4fa0-103">\_Função de \_ proxy IWICBitmapCodecInfo DoesSupportMultiframe</span><span class="sxs-lookup"><span data-stu-id="c4fa0-103">IWICBitmapCodecInfo\_DoesSupportMultiframe\_Proxy function</span></span>

<span data-ttu-id="c4fa0-104">Função de proxy para o método [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) .</span><span class="sxs-lookup"><span data-stu-id="c4fa0-104">Proxy function for the [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4fa0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4fa0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a><span data-ttu-id="c4fa0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4fa0-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="c4fa0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fa0-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="c4fa0-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="c4fa0-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="c4fa0-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="c4fa0-110">*pfSupportMultiframe* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c4fa0-110">*pfSupportMultiframe* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fa0-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="c4fa0-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="c4fa0-112">Um ponteiro que recebe _ *true*\* se o codec dá suporte a imagens de vários quadros; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="c4fa0-112">A pointer that receives _ *TRUE*\* if the codec supports multi frame images; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4fa0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4fa0-113">Return value</span></span>

<span data-ttu-id="c4fa0-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4fa0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c4fa0-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4fa0-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4fa0-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4fa0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4fa0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4fa0-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c4fa0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4fa0-118">Requirements</span></span>



| <span data-ttu-id="c4fa0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4fa0-119">Requirement</span></span> | <span data-ttu-id="c4fa0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c4fa0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fa0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4fa0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4fa0-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4fa0-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c4fa0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4fa0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c4fa0-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4fa0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c4fa0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c4fa0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4fa0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4fa0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




