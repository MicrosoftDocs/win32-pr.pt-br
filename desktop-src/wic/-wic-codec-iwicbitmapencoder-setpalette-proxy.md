---
description: Função de proxy para o método SetPalette.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: Função IWICBitmapEncoder_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 128953cd56c3bea17ec9761a2acf2b8bc89cacfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501614"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="33046-103">Função de proxy de IWICBitmapEncoder \_ Onpalette \_</span><span class="sxs-lookup"><span data-stu-id="33046-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="33046-104">Função de proxy para o método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="33046-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33046-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33046-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="33046-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33046-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="33046-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33046-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="33046-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="33046-109">Ponteiro para este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="33046-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="33046-110">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33046-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33046-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="33046-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="33046-112">O [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) a ser usado como a paleta global.</span><span class="sxs-lookup"><span data-stu-id="33046-112">The [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33046-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33046-113">Return value</span></span>

<span data-ttu-id="33046-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="33046-114">Type: **HRESULT**</span></span>

<span data-ttu-id="33046-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33046-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33046-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33046-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33046-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="33046-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="33046-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33046-118">Requirements</span></span>



| <span data-ttu-id="33046-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33046-119">Requirement</span></span> | <span data-ttu-id="33046-120">Valor</span><span class="sxs-lookup"><span data-stu-id="33046-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33046-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33046-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33046-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33046-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="33046-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33046-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33046-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33046-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="33046-125">DLL</span><span class="sxs-lookup"><span data-stu-id="33046-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33046-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33046-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




