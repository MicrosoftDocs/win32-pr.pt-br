---
description: Função de proxy para o método getstride.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: Função IWICBitmapLock_GetStride_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796152"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a><span data-ttu-id="57c2f-103">\_Função de proxy Getstride IWICBitmapLock \_</span><span class="sxs-lookup"><span data-stu-id="57c2f-103">IWICBitmapLock\_GetStride\_Proxy function</span></span>

<span data-ttu-id="57c2f-104">Função de proxy para o método [**getstride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) .</span><span class="sxs-lookup"><span data-stu-id="57c2f-104">Proxy function for the [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57c2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57c2f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a><span data-ttu-id="57c2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57c2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57c2f-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="57c2f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c2f-108">Tipo: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="57c2f-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="57c2f-109">Ponteiro para este objeto [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="57c2f-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="57c2f-110">*pcbStride* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="57c2f-110">*pcbStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57c2f-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="57c2f-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="57c2f-112">O stride do bitmap.</span><span class="sxs-lookup"><span data-stu-id="57c2f-112">The bitmap stride.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57c2f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57c2f-113">Return value</span></span>

<span data-ttu-id="57c2f-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="57c2f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="57c2f-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="57c2f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57c2f-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57c2f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57c2f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="57c2f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="57c2f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57c2f-118">Requirements</span></span>



| <span data-ttu-id="57c2f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="57c2f-119">Requirement</span></span> | <span data-ttu-id="57c2f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="57c2f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57c2f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57c2f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57c2f-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57c2f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="57c2f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57c2f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57c2f-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57c2f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="57c2f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="57c2f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57c2f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57c2f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




