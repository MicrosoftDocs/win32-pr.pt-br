---
description: Função de proxy para o método getfriendlyname.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: Função IWICComponentInfo_GetFriendlyName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764444"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a><span data-ttu-id="9cfa8-103">\_Função de proxy IWICComponentInfo Getfriendlyname \_</span><span class="sxs-lookup"><span data-stu-id="9cfa8-103">IWICComponentInfo\_GetFriendlyName\_Proxy function</span></span>

<span data-ttu-id="9cfa8-104">Função de proxy para o método [**Getfriendlyname**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .</span><span class="sxs-lookup"><span data-stu-id="9cfa8-104">Proxy function for the [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cfa8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cfa8-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="9cfa8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cfa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cfa8-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="9cfa8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cfa8-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9cfa8-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="9cfa8-109">Ponteiro para este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="9cfa8-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9cfa8-110">*cchFriendlyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cfa8-110">*cchFriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cfa8-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9cfa8-111">Type: **UINT**</span></span>

<span data-ttu-id="9cfa8-112">O tamanho do buffer *wzFriendlyName* .</span><span class="sxs-lookup"><span data-stu-id="9cfa8-112">The size of the *wzFriendlyName* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9cfa8-113">*wzFriendlyName* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9cfa8-113">*wzFriendlyName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cfa8-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9cfa8-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="9cfa8-115">Um ponteiro que recebe o nome amigável do componente.</span><span class="sxs-lookup"><span data-stu-id="9cfa8-115">A pointer that receives the friendly name of the component.</span></span>

<span data-ttu-id="9cfa8-116">A cadeia de caracteres retornada é específica da localidade, 1033 por padrão.</span><span class="sxs-lookup"><span data-stu-id="9cfa8-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="9cfa8-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9cfa8-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cfa8-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="9cfa8-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="9cfa8-119">Um ponteiro que recebe o comprimento real do nome amigável do componente.</span><span class="sxs-lookup"><span data-stu-id="9cfa8-119">A pointer that receives the actual length of the component's friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cfa8-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cfa8-120">Return value</span></span>

<span data-ttu-id="9cfa8-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9cfa8-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9cfa8-122">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9cfa8-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9cfa8-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9cfa8-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cfa8-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cfa8-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9cfa8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cfa8-125">Requirements</span></span>



| <span data-ttu-id="9cfa8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cfa8-126">Requirement</span></span> | <span data-ttu-id="9cfa8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9cfa8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cfa8-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cfa8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9cfa8-129">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cfa8-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9cfa8-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cfa8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9cfa8-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9cfa8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9cfa8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9cfa8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cfa8-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cfa8-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




