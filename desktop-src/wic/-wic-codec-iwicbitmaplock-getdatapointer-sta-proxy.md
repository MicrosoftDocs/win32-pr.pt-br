---
description: Função de proxy para o método getdatapointr.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: Função IWICBitmapLock_GetDataPointer_STA_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759818"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a><span data-ttu-id="6efeb-103">\_Função de proxy IWICBitmapLock Getdatapointr \_ STA \_</span><span class="sxs-lookup"><span data-stu-id="6efeb-103">IWICBitmapLock\_GetDataPointer\_STA\_Proxy function</span></span>

<span data-ttu-id="6efeb-104">Função de proxy para o método [**Getdatapointr**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .</span><span class="sxs-lookup"><span data-stu-id="6efeb-104">Proxy function for the [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6efeb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6efeb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a><span data-ttu-id="6efeb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6efeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6efeb-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6efeb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6efeb-108">Tipo: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="6efeb-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="6efeb-109">Ponteiro para este objeto [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="6efeb-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="6efeb-110">*pcbBufferSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6efeb-110">*pcbBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efeb-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="6efeb-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="6efeb-112">Um ponteiro que recebe o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="6efeb-112">A pointer that receives the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6efeb-113">_ppbData \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6efeb-113">_ppbData\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efeb-114">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="6efeb-114">Type: **BYTE\*\***</span></span>

<span data-ttu-id="6efeb-115">Um ponteiro que recebe um ponteiro para o pixel superior esquerdo no retângulo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6efeb-115">A pointer that receives a pointer to the top left pixel in the locked rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6efeb-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6efeb-116">Return value</span></span>

<span data-ttu-id="6efeb-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6efeb-117">Type: **HRESULT**</span></span>

<span data-ttu-id="6efeb-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6efeb-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6efeb-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6efeb-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6efeb-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6efeb-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6efeb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6efeb-121">Requirements</span></span>



| <span data-ttu-id="6efeb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6efeb-122">Requirement</span></span> | <span data-ttu-id="6efeb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6efeb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6efeb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6efeb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6efeb-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6efeb-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6efeb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6efeb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6efeb-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6efeb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6efeb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6efeb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6efeb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6efeb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




