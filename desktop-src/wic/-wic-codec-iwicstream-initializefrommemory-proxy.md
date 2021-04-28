---
description: Função de proxy de função IWICStream_InitializeFromMemory_Proxy para o método InitializeFromMemory.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: Função IWICStream_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097124"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="bf8e4-103">\_Função de \_ proxy IWICStream InitializeFromMemory</span><span class="sxs-lookup"><span data-stu-id="bf8e4-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="bf8e4-104">Função de proxy para o método [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="bf8e4-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8e4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf8e4-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="bf8e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf8e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8e4-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="bf8e4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8e4-108">Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span><span class="sxs-lookup"><span data-stu-id="bf8e4-108">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span></span>

<span data-ttu-id="bf8e4-109">Ponteiro para este objeto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="bf8e4-109">Pointer to this [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="bf8e4-110">*pbBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf8e4-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8e4-111">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="bf8e4-111">Type: **BYTE\***</span></span>

<span data-ttu-id="bf8e4-112">Ponteiro para o buffer usado para inicializar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="bf8e4-113">*cbBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf8e4-113">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8e4-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bf8e4-114">Type: **DWORD**</span></span>

<span data-ttu-id="bf8e4-115">O tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8e4-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bf8e4-116">Return value</span></span>

<span data-ttu-id="bf8e4-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf8e4-117">Type: **HRESULT**</span></span>

<span data-ttu-id="bf8e4-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bf8e4-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf8e4-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf8e4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8e4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf8e4-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bf8e4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf8e4-121">Requirements</span></span>



| <span data-ttu-id="bf8e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf8e4-122">Requirement</span></span> | <span data-ttu-id="bf8e4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bf8e4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8e4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf8e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bf8e4-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf8e4-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bf8e4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf8e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bf8e4-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf8e4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bf8e4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bf8e4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf8e4-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf8e4-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




