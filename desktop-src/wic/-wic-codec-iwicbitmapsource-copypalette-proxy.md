---
description: Função de proxy para o método CopyPalette.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: Função IWICBitmapSource_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 792738a6be3966e898527c357c99a8cd6c5cfdb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764532"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="d5f7b-103">\_Função de \_ proxy IWICBitmapSource CopyPalette</span><span class="sxs-lookup"><span data-stu-id="d5f7b-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="d5f7b-104">Função de proxy para o método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="d5f7b-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5f7b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="d5f7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5f7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f7b-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="d5f7b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f7b-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="d5f7b-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="d5f7b-109">Ponteiro para este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="d5f7b-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="d5f7b-110">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5f7b-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f7b-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="d5f7b-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="d5f7b-112">A paleta.</span><span class="sxs-lookup"><span data-stu-id="d5f7b-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f7b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5f7b-113">Return value</span></span>

<span data-ttu-id="d5f7b-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d5f7b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d5f7b-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d5f7b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5f7b-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5f7b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f7b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5f7b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f7b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5f7b-118">Requirements</span></span>



| <span data-ttu-id="d5f7b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f7b-119">Requirement</span></span> | <span data-ttu-id="d5f7b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d5f7b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f7b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5f7b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f7b-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5f7b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d5f7b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5f7b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f7b-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5f7b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d5f7b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f7b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f7b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5f7b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




