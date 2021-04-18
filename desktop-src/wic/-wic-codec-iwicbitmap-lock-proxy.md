---
description: Função de proxy para o método Lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: Função IWICBitmap_Lock_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810191"
---
# <a name="iwicbitmap_lock_proxy-function"></a><span data-ttu-id="80bd3-103">Função de proxy de \_ bloqueio IWICBitmap \_</span><span class="sxs-lookup"><span data-stu-id="80bd3-103">IWICBitmap\_Lock\_Proxy function</span></span>

<span data-ttu-id="80bd3-104">Função de proxy para o método [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) .</span><span class="sxs-lookup"><span data-stu-id="80bd3-104">Proxy function for the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80bd3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80bd3-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a><span data-ttu-id="80bd3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80bd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80bd3-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="80bd3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bd3-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="80bd3-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="80bd3-109">Ponteiro para este objeto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="80bd3-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="80bd3-110">*prcLock* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80bd3-110">*prcLock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bd3-111">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="80bd3-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="80bd3-112">O retângulo a ser acessado.</span><span class="sxs-lookup"><span data-stu-id="80bd3-112">The rectangle to be accessed.</span></span>

</dd> <dt>

<span data-ttu-id="80bd3-113">_flags \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80bd3-113">_flags\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bd3-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="80bd3-114">Type: **DWORD**</span></span>

<span data-ttu-id="80bd3-115">O modo de acesso que você deseja obter para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="80bd3-115">The access mode you wish to obtain for the lock.</span></span>

</dd> <dt>

<span data-ttu-id="80bd3-116">*ppILock* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="80bd3-116">*ppILock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80bd3-117">Tipo: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span><span class="sxs-lookup"><span data-stu-id="80bd3-117">Type: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span></span>

<span data-ttu-id="80bd3-118">Um ponteiro que recebe o local da memória bloqueada.</span><span class="sxs-lookup"><span data-stu-id="80bd3-118">A pointer that receives the locked memory location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80bd3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80bd3-119">Return value</span></span>

<span data-ttu-id="80bd3-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="80bd3-120">Type: **HRESULT**</span></span>

<span data-ttu-id="80bd3-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80bd3-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80bd3-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80bd3-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80bd3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="80bd3-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="80bd3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80bd3-124">Requirements</span></span>



| <span data-ttu-id="80bd3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80bd3-125">Requirement</span></span> | <span data-ttu-id="80bd3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="80bd3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bd3-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80bd3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80bd3-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80bd3-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="80bd3-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80bd3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80bd3-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80bd3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="80bd3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="80bd3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80bd3-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80bd3-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




