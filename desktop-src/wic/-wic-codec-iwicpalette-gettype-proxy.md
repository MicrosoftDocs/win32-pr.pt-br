---
description: Função de proxy para o método GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: Função IWICPalette_GetType_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771387"
---
# <a name="iwicpalette_gettype_proxy-function"></a><span data-ttu-id="cd904-103">\_Função de \_ proxy IWICPalette GetType</span><span class="sxs-lookup"><span data-stu-id="cd904-103">IWICPalette\_GetType\_Proxy function</span></span>

<span data-ttu-id="cd904-104">Função de proxy para o método [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .</span><span class="sxs-lookup"><span data-stu-id="cd904-104">Proxy function for the [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd904-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd904-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a><span data-ttu-id="cd904-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd904-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd904-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="cd904-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd904-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="cd904-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="cd904-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="cd904-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="cd904-110">*pePaletteType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cd904-110">*pePaletteType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd904-111">Tipo: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _</span><span class="sxs-lookup"><span data-stu-id="cd904-111">Type: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\** _</span></span>

<span data-ttu-id="cd904-112">Ponteiro que recebe o tipo de paleta do bimtap.</span><span class="sxs-lookup"><span data-stu-id="cd904-112">Pointer that receives the palette type of the bimtap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd904-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd904-113">Return value</span></span>

<span data-ttu-id="cd904-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cd904-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cd904-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cd904-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd904-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd904-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd904-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd904-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cd904-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd904-118">Requirements</span></span>



| <span data-ttu-id="cd904-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd904-119">Requirement</span></span> | <span data-ttu-id="cd904-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cd904-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd904-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd904-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cd904-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd904-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cd904-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd904-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cd904-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd904-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cd904-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cd904-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd904-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd904-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




