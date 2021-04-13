---
description: Função de proxy para o método SetPalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: Função IWICBitmap_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501618"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="eb329-103">\_Função de proxy SetPalette IWICBitmap \_</span><span class="sxs-lookup"><span data-stu-id="eb329-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="eb329-104">Função de proxy para o método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="eb329-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb329-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb329-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="eb329-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb329-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb329-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="eb329-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb329-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="eb329-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="eb329-109">Ponteiro para este objeto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="eb329-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="eb329-110">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb329-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb329-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="eb329-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="eb329-112">A paleta a ser usada para conversão.</span><span class="sxs-lookup"><span data-stu-id="eb329-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb329-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb329-113">Return value</span></span>

<span data-ttu-id="eb329-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="eb329-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="eb329-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb329-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb329-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb329-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb329-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb329-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="eb329-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb329-118">Requirements</span></span>



| <span data-ttu-id="eb329-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb329-119">Requirement</span></span> | <span data-ttu-id="eb329-120">Valor</span><span class="sxs-lookup"><span data-stu-id="eb329-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb329-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb329-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eb329-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb329-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="eb329-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb329-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eb329-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eb329-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="eb329-125">DLL</span><span class="sxs-lookup"><span data-stu-id="eb329-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb329-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb329-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




