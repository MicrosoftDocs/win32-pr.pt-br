---
description: Função de proxy para o método GetCLSID.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: Função IWICComponentInfo_GetCLSID_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc63d3f30605c0f5343502bcb96e989cc8496540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793248"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a><span data-ttu-id="3468d-103">\_Função de proxy GetCLSID IWICComponentInfo \_</span><span class="sxs-lookup"><span data-stu-id="3468d-103">IWICComponentInfo\_GetCLSID\_Proxy function</span></span>

<span data-ttu-id="3468d-104">Função de proxy para o método [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) .</span><span class="sxs-lookup"><span data-stu-id="3468d-104">Proxy function for the [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3468d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3468d-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a><span data-ttu-id="3468d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3468d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3468d-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="3468d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3468d-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3468d-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="3468d-109">Ponteiro para este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="3468d-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="3468d-110">*pCLSID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3468d-110">*pclsid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3468d-111">Tipo: \**CLSID \** _</span><span class="sxs-lookup"><span data-stu-id="3468d-111">Type: \**CLSID\** _</span></span>

<span data-ttu-id="3468d-112">Um ponteiro que recebe o CLSID do componente.</span><span class="sxs-lookup"><span data-stu-id="3468d-112">A pointer that receives the component's CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3468d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3468d-113">Return value</span></span>

<span data-ttu-id="3468d-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3468d-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3468d-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3468d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3468d-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3468d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3468d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3468d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3468d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3468d-118">Requirements</span></span>



| <span data-ttu-id="3468d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3468d-119">Requirement</span></span> | <span data-ttu-id="3468d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3468d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3468d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3468d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3468d-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3468d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3468d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3468d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3468d-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3468d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3468d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3468d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3468d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3468d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




