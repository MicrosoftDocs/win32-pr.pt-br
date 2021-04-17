---
description: Função de proxy para o método GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: Função IWICComponentInfo_GetVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771359"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a><span data-ttu-id="4a4a1-103">\_Função de proxy GetVersion do IWICComponentInfo \_</span><span class="sxs-lookup"><span data-stu-id="4a4a1-103">IWICComponentInfo\_GetVersion\_Proxy function</span></span>

<span data-ttu-id="4a4a1-104">Função de proxy para o método [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .</span><span class="sxs-lookup"><span data-stu-id="4a4a1-104">Proxy function for the [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a4a1-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="4a4a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a4a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4a1-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="4a4a1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4a1-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="4a4a1-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="4a4a1-109">Ponteiro para este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="4a4a1-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="4a4a1-110">*cchVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a4a1-110">*cchVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4a1-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4a4a1-111">Type: **UINT**</span></span>

<span data-ttu-id="4a4a1-112">O tamanho do buffer *wzVersion* .</span><span class="sxs-lookup"><span data-stu-id="4a4a1-112">The size of the *wzVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4a4a1-113">*wzVersion* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4a4a1-113">*wzVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4a1-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="4a4a1-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="4a4a1-115">Um ponteiro que recebe uma cadeia de caracteres invariável de cultura da versão do componente.</span><span class="sxs-lookup"><span data-stu-id="4a4a1-115">A pointer that receives a culture invariant string of the component's version.</span></span>

</dd> <dt>

<span data-ttu-id="4a4a1-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4a4a1-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4a1-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="4a4a1-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="4a4a1-118">Um ponteiro que recebe o comprimento real da versão do componente.</span><span class="sxs-lookup"><span data-stu-id="4a4a1-118">A pointer that receives the actual length of the component's version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a4a1-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a4a1-119">Return value</span></span>

<span data-ttu-id="4a4a1-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4a4a1-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4a4a1-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a4a1-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a4a1-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a4a1-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a4a1-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a4a1-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4a1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a4a1-124">Requirements</span></span>



| <span data-ttu-id="4a4a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a4a1-125">Requirement</span></span> | <span data-ttu-id="4a4a1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4a4a1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4a1-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a4a1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4a1-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a4a1-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4a4a1-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a4a1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4a1-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a4a1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4a4a1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4a4a1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a4a1-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a4a1-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




