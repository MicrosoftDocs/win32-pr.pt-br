---
description: Função de proxy de função IWICColorContext_InitializeFromMemory_Proxy para o método InitializeFromMemory.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: Função IWICColorContext_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e77bbcf1e430891b031b2e77bc168c33f781eacf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097214"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="2517c-103">\_Função de \_ proxy IWICColorContext InitializeFromMemory</span><span class="sxs-lookup"><span data-stu-id="2517c-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="2517c-104">Função de proxy para o método [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="2517c-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2517c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2517c-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="2517c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2517c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2517c-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="2517c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2517c-108">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="2517c-108">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

</dd> <dt>

<span data-ttu-id="2517c-109">*pbBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2517c-109">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2517c-110">Tipo: **byte \* const**</span><span class="sxs-lookup"><span data-stu-id="2517c-110">Type: **const BYTE\***</span></span>

<span data-ttu-id="2517c-111">O buffer usado para inicializar o [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="2517c-111">The buffer used to initialize the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="2517c-112">*cbBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2517c-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2517c-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2517c-113">Type: **UINT**</span></span>

<span data-ttu-id="2517c-114">O tamanho do buffer *pbBuffer* .</span><span class="sxs-lookup"><span data-stu-id="2517c-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2517c-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2517c-115">Return value</span></span>

<span data-ttu-id="2517c-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2517c-116">Type: **HRESULT**</span></span>

<span data-ttu-id="2517c-117">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2517c-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2517c-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2517c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2517c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2517c-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2517c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2517c-120">Requirements</span></span>



| <span data-ttu-id="2517c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2517c-121">Requirement</span></span> | <span data-ttu-id="2517c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2517c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2517c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2517c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2517c-124">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2517c-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2517c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2517c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2517c-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2517c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2517c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2517c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2517c-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2517c-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




